---
title: Liberare i descrittori WinSNMP
description: L'ambiente di programmazione WinSNMP assegna la deallocazione delle risorse del descrittore all'implementazione WinSNMP o all'applicazione WinSNMP, a seconda del componente che alloca la memoria per il descrittore.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009529"
---
# <a name="freeing-winsnmp-descriptors"></a>Liberare i descrittori WinSNMP

L'ambiente di programmazione WinSNMP assegna la deallocazione delle risorse del descrittore all'implementazione WinSNMP o all'applicazione WinSNMP, a seconda del componente che alloca la memoria per il descrittore.

Per liberare le risorse per [**un descrittore smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) si applicano le regole seguenti:

-   Per i parametri di input

    Poiché l'applicazione WinSNMP alloca la memoria per gli oggetti di input con lunghezze variabili, l'applicazione deve liberare tale memoria usando una funzione appropriata. Ad esempio, se l'applicazione ha allocato le risorse con una chiamata alla [**funzione GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) deve usare la [**funzione GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) per deallocare le risorse. Se l'applicazione ha allocato le risorse con una chiamata alla [**funzione HeapAlloc,**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) deve chiamare la [**funzione HeapFree.**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)

-   Per i parametri di output

    Una chiamata a una delle funzioni seguenti comporta l'implementazione dell'allocazione di memoria per [**un descrittore smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS:**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) [**SnmpGetVb,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) [**SnmpEncodeMsg,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) [**SnmpOidCopy,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)e [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Poiché l'implementazione alloca la memoria per questi oggetti di output, l'applicazione deve chiamare la [**funzione SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per deallocare le risorse. Questa funzione consente all'implementazione di liberare la memoria allocata per il membro **ptr** di queste strutture.

Per liberare le risorse per una [**struttura smiVALUE,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) un'applicazione WinSNMP deve controllare  il membro della sintassi di una [**struttura smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) per valutare correttamente il membro valore della struttura.  Se  il membro della  sintassi indica che il membro valore è [**un descrittore smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) e l'implementazione ha allocato le risorse per il descrittore, l'applicazione deve chiamare [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Ciò consente all'implementazione di liberare la memoria. Se l'applicazione ha allocato le risorse, deve liberare la memoria usando una funzione appropriata, come indicato in precedenza.

Per altre informazioni, vedere [Allocazione di oggetti di memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 