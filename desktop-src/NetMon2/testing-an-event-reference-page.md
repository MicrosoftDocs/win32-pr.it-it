---
description: Il passaggio finale della creazione di una pagina di riferimento a un evento consiste nel testarlo.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Test di una pagina di riferimento a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307820"
---
# <a name="testing-an-event-reference-page"></a>Test di una pagina di riferimento a un evento

Il passaggio finale della creazione di una pagina di riferimento a un evento consiste nel testarlo. È possibile testare un ERP visualizzando il file in un browser HTML, ad esempio Microsoft Internet Explorer. In alternativa, è possibile installare il ERP e la relativa DLL di esperti per testarla per la chiamata di un evento e visualizzarla nel Visualizzatore eventi Network Monitor.

## <a name="viewing-erps-that-have-no-dll"></a>Visualizzazione di ERPs senza DLL

Per visualizzare il ERP completato senza una DLL di esperti installata, aprire il file con un visualizzatore HTML che supporta le origini incorporate. Nella figura seguente viene illustrato il file ERP di esempio descritto in [scrittura di un ERP](writing-an-event-reference-page.md) così come viene visualizzato con Microsoft Internet Explorer versione 4,01.

![file ERP di esempio](images/ie-erp.png)

Test di ERPs con una DLL

Dopo aver creato i file ERP e la dll di [**esperti**](experts.md) , è possibile testare la funzionalità completa del ERPs con Network Monitor. Si presuppone che la DLL sia sottoposta a debug e che sia in grado di generare eventi validi.

**Per testare ERPs che contengono una DLL**

1.  Verificare che nella directory appropriata sia installata la DLL Expert corretta. Per ulteriori informazioni, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Verificare il [nome corretto](naming-an-event-reference-page.md) del file ERP.
3.  Verificare il [percorso corretto](installing-existing-erps-to-network-monitor-2-1.md) di Erps nella directory Network Monitor.
4.  ERPs esperto test nell'interfaccia utente di Network Monitor.
5.  Genera un evento di test.
6.  Verificare che il ERP venga visualizzato nell'Visualizzatore eventi Network Monitor.

Per ulteriori informazioni sulla creazione di un ERP, vedere:

-   [Creazione di pagine di riferimento per gli eventi Expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Scrittura di una pagina di riferimento a un evento](writing-an-event-reference-page.md)
-   [Denominazione di una pagina di riferimento a un evento](naming-an-event-reference-page.md)

 

 



