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
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="2740d-104">Implementazione di ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="2740d-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="2740d-105">Network Monitor usa la funzione di esportazione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) per installare un parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="2740d-106">Quando viene chiamato **ParserAutoInstallInfo** , il parser restituisce una struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) contenente tutte le informazioni che Network Monitor necessario installare una dll del parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="2740d-107">Network Monitor mantiene un elenco di parser esistenti nel file di [*Parser.ini*](p.md) e crea un file ini separato per ogni parser installato.</span><span class="sxs-lookup"><span data-stu-id="2740d-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="2740d-108">Durante il processo di installazione, la DLL del parser deve identificare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2740d-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="2740d-109">Numero di parser nella DLL, inclusi un nome e una descrizione di commento per ogni parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="2740d-110">Protocolli che precedono il protocollo del parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="2740d-111">Protocolli che seguono il protocollo del parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="2740d-112">Network Monitor usa le informazioni sul protocollo del parser precedenti e seguenti per aggiornare i [*set di continuità*](h.md) e [*seguire i set*](f.md) di parser identificati dalla dll del parser.</span><span class="sxs-lookup"><span data-stu-id="2740d-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="2740d-113">Nella procedura seguente vengono identificati i passaggi necessari per implementare [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="2740d-114">**Per implementare ParserAutoInstallInfo**</span><span class="sxs-lookup"><span data-stu-id="2740d-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="2740d-115">Allocare una struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="2740d-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="2740d-116">Restituire memoria all'heap utilizzando **HeapFree**.</span><span class="sxs-lookup"><span data-stu-id="2740d-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="2740d-117">Tenere presente che questa chiamata deve allocare anche una struttura [**PF \_ PARSERINFO**](pf-parserinfo.md) per ogni parser della dll.</span><span class="sxs-lookup"><span data-stu-id="2740d-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="2740d-118">Specificare il numero di parser (in genere uno) che la DLL contiene nel membro **nParsers** di [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="2740d-119">Specificare un nome, un commento e un file della guida facoltativo nei membri **szProtocolName**, **szComment** e **szHelpFile** di ogni struttura [**PF \_ PARSERINFO**](pf-parserinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2740d-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="2740d-120">Specificare i protocolli che precedono ogni protocollo DLL.</span><span class="sxs-lookup"><span data-stu-id="2740d-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="2740d-121">Una delle condizioni seguenti si applica a un set di continuità in ingresso.</span><span class="sxs-lookup"><span data-stu-id="2740d-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="2740d-122">Se i protocolli precedenti possono determinare che il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoHandsOffToMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="2740d-123">In questo caso, il protocollo viene aggiunto ai set di [*continuità*](h.md) dei protocolli precedenti.</span><span class="sxs-lookup"><span data-stu-id="2740d-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="2740d-124">Se i protocolli precedenti non possono determinare se il protocollo segue i dati nei protocolli precedenti, impostare il membro **pWhoCanPrecedeMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="2740d-125">In questo caso, il protocollo viene aggiunto ai set di protocolli [*seguenti*](f.md) .</span><span class="sxs-lookup"><span data-stu-id="2740d-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="2740d-126">Specificare i protocolli che seguono ogni protocollo DLL.</span><span class="sxs-lookup"><span data-stu-id="2740d-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="2740d-127">Una delle condizioni seguenti si applica a un set di seguito in uscita.</span><span class="sxs-lookup"><span data-stu-id="2740d-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="2740d-128">Se il protocollo può determinare quali protocolli seguono in base ai dati nel protocollo, impostare il membro **pWhoDoIHandOffTo** di [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="2740d-129">In questo caso, questi protocolli vengono aggiunti al set di [*continuità*](h.md) dei protocolli.</span><span class="sxs-lookup"><span data-stu-id="2740d-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="2740d-130">Se il protocollo non è in grado di determinare i protocolli che seguono in base ai dati nel protocollo, impostare il membro **pWhoCanFollowMe** di [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="2740d-131">In questo caso, questi protocolli vengono aggiunti al set di protocolli [*seguente*](f.md) .</span><span class="sxs-lookup"><span data-stu-id="2740d-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="2740d-132">Restituisce la struttura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) per Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="2740d-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="2740d-133">Di seguito è riportata un'implementazione di base di [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2740d-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="2740d-134">L'esempio di codice viene tratto dal parser generico fornito da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="2740d-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

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

 

 



