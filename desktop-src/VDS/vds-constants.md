---
description: Costanti VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Costanti VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9fa0c6196e1085de3a5433750b890e2ad3bc42f4a86022587f02157521eacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125694"
---
# <a name="vds-constants"></a>Costanti VDS

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Le costanti VDS sono classificate come segue:

-   [Costanti di stato dell'oggetto](#object-status-constants)
-   [Costanti dei suggerimenti automagic](#automagic-hints-constants)
-   [Costanti varie](#miscellaneous-constants)

### <a name="object-status-constants"></a>Costanti di stato dell'oggetto



| Costante           | Valore |
|--------------------|-------|
| STATO \_ SCONOSCIUTO    | 0     |
| STATO \_ ONLINE     | 1     |
| STATO \_ NON \_ PRONTO | 2     |
| STATO \_ NO \_ MEDIA  | 3     |
| STATO \_ OFFLINE    | 4     |
| STATO \_ NON RIUSCITO     | 5     |
| STATO \_ MANCANTE    | 6     |



 

### <a name="automagic-hints-constants"></a>Costanti dei suggerimenti automagic



| Costante                               | Valore   |
|----------------------------------------|---------|
| HINT VDS \_ \_ PRINCIPALMENTEREADS                 | 0x0002L |
| OTTIMIZZAZIONE \_ HINT \_ VDSFORSEQUENTIALREADS  | 0x0004L |
| OTTIMIZZAZIONE \_ HINT \_ VDSFORSEQUENTIALWRITES | 0x0008L |
| \_REMAPENABLED DELL'HINT \_ VDS                | 0x0020L |
| \_WRITETHROUGHCACHINGENABLED DELL'HINT VDS \_  | 0x0040L |
| SUGGERIMENTO VDS \_ \_ HARDWARECHECKSUMENABLED     | 0x0080L |
| VDS \_ HINT \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Costanti varie



| Costante                     | Valore      |
|------------------------------|------------|
| PRIORITÀ DI \_ \_ RICOMPILAZIONE VDS \_ MIN  | 0x0001L    |
| INFORMAZIONI SUL LUN VER \_ VDS \_ \_   | 1          |
| LUNGHEZZA \_ MASSIMA \_ COMPUTERNAME    | 15         |
| LUNGHEZZA \_ MASSIMA \_ PROVIDERNAME    | 200        |
| LUNGHEZZA \_ MASSIMA \_ VERSIONSTRING   | 16         |
| PROP \_ LETTERA \_ DI UNITÀ          | N/A        |
| DIMENSIONI \_ MASSIME \_ DEI NOMI \_ FS          | 8          |
| IDX \_ \_ MEMBRO NON VALIDO         | 0xffffffff |
| LUNGHEZZA NOME PARTIZIONE GPT \_ \_ \_ | 36         |
| MAX \_ PATH                    | 260        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su VDS](vds-reference.md)
</dt> </dl>

 

 
