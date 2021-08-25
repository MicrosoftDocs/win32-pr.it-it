---
title: Flag di enumerazione
description: Flag di enumerazione
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumerazione
- Flag di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa99352db877cdaef3d5297d754d1e66bb246240074cfc741ba3baff94a5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910271"
---
# <a name="enumeration-flags"></a>Flag di enumerazione



| Costante               | Valore      | Descrizione                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVVIO \_ DELL'ENUMERAZIONE RTM \_       | 0x00000000 | Enumerare le route o le destinazioni a partire da 0/0.                                                                                                         |
| RTM \_ ENUM \_ NEXT        | 0x00000001 | Enumera le route o le destinazioni a partire dalla lunghezza di indirizzo/maschera specificata, ad esempio 10/8. L'enumerazione continua fino alla fine della tabella di routing. |
| INTERVALLO DI ENUMERAZIONE RTM \_ \_       | 0x00000002 | Enumera le route o le destinazioni nel sottoalbero specificato dalla lunghezza di indirizzo/maschera (ad esempio 10/8).                                            |
| ENUMERAZIONE RTM \_ \_ ALL \_ DESTS  | 0x00000000 | Restituisce tutte le destinazioni.                                                                                                                                  |
| DESTS \_ DI ENUMERAZIONE RTM \_ \_  | 0x01000000 | Restituire solo le destinazioni di proprietà del client.                                                                                                      |
| ENUMERAZIONE RTM \_ \_ TUTTE LE \_ ROUTE | 0x00000000 | Restituisce tutte le route.                                                                                                                                        |
| ROUTE \_ PROPRIE DELL'ENUMERAZIONE RTM \_ \_ | 0x00010000 | Restituisce solo le route di proprietà del client.                                                                                                            |



 

 

 




