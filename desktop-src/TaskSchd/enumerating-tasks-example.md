---
title: Esempio di attività di enumerazione
description: Per enumerare le attività, è necessario chiamare l'enumerazione ITaskScheduler per creare un oggetto di enumerazione. Utilizzare quindi l'interfaccia IEnumWorkItems dell'oggetto enumerazione per enumerare le attività nella cartella delle attività pianificate.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300204"
---
# <a name="enumerating-tasks-example"></a>Esempio di attività di enumerazione

Per enumerare le attività, è necessario chiamare [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) per creare un [*oggetto di enumerazione*](e.md). Utilizzare quindi l'interfaccia [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) dell'oggetto enumerazione per enumerare le attività nella cartella delle attività pianificate.

Nella procedura riportata di seguito viene descritto come enumerare le attività nella cartella delle attività pianificate.

**Per enumerare le attività nella cartella delle attività pianificate**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) per ottenere un oggetto di enumerazione.
3.  Chiamare [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) per recuperare le attività. In questo esempio si tenta di recuperare cinque attività a ogni chiamata.
4.  Elabora le attività restituite. In questo esempio il nome di ogni attività viene semplicemente stampato sullo schermo.
5.  Rilasciare le risorse. Chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria usata per i nomi.



| Per un esempio di codice di                                                         | Vedere                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Enumerazione di tutte le attività nella cartella delle attività pianificate del computer locale | [Esempio di codice C/C++: enumerazione delle attività](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 