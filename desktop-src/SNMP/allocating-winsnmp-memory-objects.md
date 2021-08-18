---
title: Allocazione di oggetti di memoria WinSNMP
description: I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1188af74e150313cb24b01886d06df9e3ad065039cad9fa4a3e0b3b5ee6a9f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009789"
---
# <a name="allocating-winsnmp-memory-objects"></a>Allocazione di oggetti di memoria WinSNMP

I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.

Il tipo di oggetto determina se l'implementazione Microsoft WinSNMP o l'applicazione WinSNMP alloca e dealloca la memoria per l'oggetto. In questo modo si riduce l'allocazione non necessaria di spazio temporaneo nel buffer e la copia non necessaria dei buffer.

La tabella seguente riepiloga l'allocazione e la deallocazione delle risorse per gli oggetti di memoria WinSNMP.



| Tipo di oggetto                                                                   | Descrizione                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descrittore smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Se l'applicazione WinSNMP alloca la memoria, deve deallocare la memoria con una chiamata a una funzione appropriata. Se l'implementazione alloca la memoria, l'applicazione deve chiamare la [**funzione SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per deallocare la memoria. |
| [**Struttura smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Se il **membro valore** è [**un descrittore smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) l'applicazione deve procedere come indicato in precedenza per i descrittori.                                                                                                     |
| Handle di risorsa                                                               | L'implementazione alloca, gestisce e libera la memoria.                                                                                                                                                                                                                         |
| Stringa di tipo C                                                                | L'applicazione WinSNMP deve gestire e liberare la memoria allocata.                                                                                                                                                                                                                |



 

Per altre informazioni, vedere [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).

 

 




