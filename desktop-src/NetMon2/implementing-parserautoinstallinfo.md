---
description: Network Monitor usa la funzione di esportazione ParserAutoInstallInfo per installare un parser. Quando viene chiamato ParserAutoInstallInfo, il parser restituisce una struttura PF PARSERDLLINFO contenente tutte le informazioni necessarie Network Monitor installare una \_ DLL del parser.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementazione di ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743081"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementazione di ParserAutoInstallInfo

Network Monitor usa la [**funzione di esportazione ParserAutoInstallInfo**](parserautoinstallinfo.md) per installare un parser. Quando **viene chiamato ParserAutoInstallInfo,** il parser restituisce una struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) contenente tutte le informazioni necessarie Network Monitor installare una DLL del parser.

> [!Note]  
> Network Monitor un elenco di parser esistenti nel file [*Parser.ini*](p.md) e crea un file INI separato per ogni parser installato.

 

Durante il processo di installazione, la DLL del parser deve identificare quanto segue:

-   Numero di parser nella DLL, inclusi un nome e una descrizione del commento per ogni parser.
-   Protocolli che precedono il protocollo del parser.
-   Protocolli che seguono il protocollo del parser.

> [!Note]  
> Network Monitor usa le informazioni sul protocollo del parser precedenti e [](f.md) seguenti per aggiornare i set di [*handoff*](h.md) e seguire i set di parser identificati dalla DLL del parser.

 

La procedura seguente identifica i passaggi necessari per [**implementare ParserAutoInstallInfo.**](parserautoinstallinfo.md)

**Per implementare ParserAutoInstallInfo**

1.  Allocare [**una struttura PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) usando **HeapAlloc**.
2.  Restituire memoria all'heap usando **HeapFree**.
3.  Tenere presente che questa chiamata deve allocare anche una [**struttura \_ PARSERINFO PF**](pf-parserinfo.md) per ogni parser nella DLL.
4.  Specificare il numero di parser (in genere uno) contenuto nella DLL nel membro **nParsers** di [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Specificare un nome, un commento e un file della Guida facoltativo nei membri **szProtocolName**, **szComment** e **szHelpFile** di ogni [**struttura PF \_ PARSERINFO.**](pf-parserinfo.md)
6.  Specificare i protocolli che precedono ogni protocollo DLL. Una delle condizioni seguenti si applica a un set di handoff in ingresso.
    -   Se i protocolli precedenti possono determinare che il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoHandsOffToMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, il protocollo viene quindi aggiunto ai [*set di handoff*](h.md) dei protocolli precedenti.
    -   Se i protocolli precedenti non sono in grado di determinare che il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoCanPrecedeMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md). In questo caso, il protocollo viene quindi aggiunto ai [*set di*](f.md) protocolli seguenti.
7.  Specificare i protocolli che seguono ogni protocollo DLL. Una delle condizioni seguenti si applica a un follow-set in uscita.
    -   Se il protocollo può determinare quali protocolli seguono in base ai dati nel protocollo, impostare il membro **pWhoDoIHandOffTo** di [**PF \_ PARSERINFO.**](pf-parserinfo.md) In questo caso, questi protocolli vengono aggiunti al [*set di handoff*](h.md) dei protocolli.
    -   Se il protocollo non è in grado di determinare quali protocolli seguono in base ai dati nel protocollo, impostare il membro **pWhoCanFollowMe** di [**PF \_ PARSERINFO.**](pf-parserinfo.md) In questo caso, questi protocolli vengono aggiunti al [*set di protocolli*](f.md) seguente.
8.  Restituisce la [**struttura PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) Network Monitor.

Di seguito è riportata un'implementazione di [**base di ParserAutoInstallInfo.**](parserautoinstallinfo.md) L'esempio di codice è tratto dal parser generico Network Monitor fornito.

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

 

 



