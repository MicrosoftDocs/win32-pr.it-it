---
description: Network Monitor usa la funzione di esportazione ParserAutoInstallInfo per installare un parser. Quando viene chiamato ParserAutoInstallInfo, il parser restituisce una \_ struttura PF PARSERDLLINFO contenente tutte le informazioni che Network Monitor necessario installare una dll del parser.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementazione di ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317102"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementazione di ParserAutoInstallInfo

Network Monitor usa la funzione di esportazione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) per installare un parser. Quando viene chiamato **ParserAutoInstallInfo** , il parser restituisce una struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) contenente tutte le informazioni che Network Monitor necessario installare una dll del parser.

> [!Note]  
> Network Monitor mantiene un elenco di parser esistenti nel file di [*Parser.ini*](p.md) e crea un file ini separato per ogni parser installato.

 

Durante il processo di installazione, la DLL del parser deve identificare gli elementi seguenti:

-   Numero di parser nella DLL, inclusi un nome e una descrizione di commento per ogni parser.
-   Protocolli che precedono il protocollo del parser.
-   Protocolli che seguono il protocollo del parser.

> [!Note]  
> Network Monitor usa le informazioni sul protocollo del parser precedenti e seguenti per aggiornare i [*set di continuità*](h.md) e [*seguire i set*](f.md) di parser identificati dalla dll del parser.

 

Nella procedura seguente vengono identificati i passaggi necessari per implementare [**ParserAutoInstallInfo**](parserautoinstallinfo.md).

**Per implementare ParserAutoInstallInfo**

1.  Allocare una struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) usando **HeapAlloc**.
2.  Restituire memoria all'heap utilizzando **HeapFree**.
3.  Tenere presente che questa chiamata deve allocare anche una struttura [**PF \_ PARSERINFO**](pf-parserinfo.md) per ogni parser della dll.
4.  Specificare il numero di parser (in genere uno) che la DLL contiene nel membro **nParsers** di [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Specificare un nome, un commento e un file della guida facoltativo nei membri **szProtocolName**, **szComment** e **szHelpFile** di ogni struttura [**PF \_ PARSERINFO**](pf-parserinfo.md) .
6.  Specificare i protocolli che precedono ogni protocollo DLL. Una delle condizioni seguenti si applica a un set di continuità in ingresso.
    -   Se i protocolli precedenti possono determinare che il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoHandsOffToMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, il protocollo viene aggiunto ai set di [*continuità*](h.md) dei protocolli precedenti.
    -   Se i protocolli precedenti non possono determinare se il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoCanPrecedeMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, il protocollo viene aggiunto ai set di protocolli [*seguenti*](f.md) .
7.  Specificare i protocolli che seguono ogni protocollo DLL. Una delle condizioni seguenti si applica a un set di seguito in uscita.
    -   Se il protocollo può determinare quali protocolli seguono in base ai dati nel protocollo, impostare il membro **pWhoDoIHandOffTo** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, questi protocolli vengono aggiunti al set di [*continuità*](h.md) dei protocolli.
    -   Se il protocollo non è in grado di determinare i protocolli che seguono in base ai dati nel protocollo, impostare il membro **pWhoCanFollowMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, questi protocolli vengono aggiunti al set di protocolli [*seguente*](f.md) .
8.  Restituisce la struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) per Network Monitor.

Di seguito è riportata un'implementazione di base di [**ParserAutoInstallInfo**](parserautoinstallinfo.md). L'esempio di codice viene tratto dal parser generico fornito da Network Monitor.

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



