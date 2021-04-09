---
title: Allocazione di oggetti memoria WinSNMP
description: I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044040"
---
# <a name="allocating-winsnmp-memory-objects"></a>Allocazione di oggetti memoria WinSNMP

I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.

Il tipo di oggetto determina se l'implementazione di Microsoft WinSNMP o l'applicazione WinSNMP alloca e dealloca la memoria per l'oggetto. In questo modo si riduce l'allocazione non necessaria dello spazio del buffer temporaneo e la copia superflua dei buffer.

La tabella seguente riepiloga l'allocazione e la deallocazione delle risorse per gli oggetti memoria WinSNMP.



| Tipo di oggetto                                                                   | Descrizione                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Se l'applicazione WinSNMP alloca la memoria, deve deallocare la memoria con una chiamata a una funzione appropriata. Se l'implementazione alloca la memoria, l'applicazione deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per deallocare la memoria. |
| struttura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Se il membro del **valore** è un descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , l'applicazione deve continuare come indicato in precedenza per i descrittori.                                                                                                     |
| Handle di risorsa                                                               | L'implementazione alloca, gestisce e libera la memoria.                                                                                                                                                                                                                         |
| Stringa di tipo C                                                                | L'applicazione WinSNMP deve gestire e liberare la memoria allocata.                                                                                                                                                                                                                |



 

Per ulteriori informazioni, vedere la pagina relativa alla [liberazione dei descrittori WinSNMP](freeing-winsnmp-descriptors.md).

 

 




