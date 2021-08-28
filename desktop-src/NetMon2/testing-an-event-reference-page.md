---
description: Il passaggio finale della creazione di una pagina di riferimento eventi (ERP) consiste nel testarla.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Test di una pagina di riferimento eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aa9fb8697181085a9b74333dba82328e90b502e6590a764fac589efa8e6f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676637"
---
# <a name="testing-an-event-reference-page"></a>Test di una pagina di riferimento eventi

Il passaggio finale della creazione di una pagina di riferimento eventi (ERP) consiste nel testarla. È possibile testare un ERP visualizzando il file in un browser HTML, ad esempio Microsoft Internet Explorer. In caso contrario, è possibile installare ERP e la relativa DLL esperta per testarla per la chiamata all'evento e visualizzarla nel Network Monitor Visualizzatore eventi.

## <a name="viewing-erps-that-have-no-dll"></a>Visualizzazione di file ERP senza DLL

Per visualizzare il file ERP completato senza una DLL esperta installata, aprire il file con un visualizzatore HTML che supporta le origini incorporate. La figura seguente mostra il file ERP di esempio descritto in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer version 4.01 (Scrittura di un ERP così come viene visualizzato con Microsoft Internet Explorer versione 4.01).

![file erp di esempio](images/ie-erp.png)

Test degli EERP con una DLL

Dopo aver creato i file ERP e [**la**](experts.md) DLL esperta, è possibile testare la funzionalità completa dei file ERP con Network Monitor. Si presuppone che la DLL sia in fase di debug e possa generare eventi validi.

**Per testare gli EERP con una DLL**

1.  Verificare che la DLL esperta corretta sia installata nella directory appropriata. Per altre informazioni, vedere [Installazione di un esperto Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).
2.  Verificare il [nome corretto](naming-an-event-reference-page.md) del file ERP.
3.  Verificare il [percorso corretto](installing-existing-erps-to-network-monitor-2-1.md) dei file ERP nella directory Network Monitor.
4.  Eseguire test di EERP esperti nell'interfaccia Network Monitor interfaccia utente.
5.  Generare un evento di test.
6.  Verificare che il componente ERP sia visualizzato nel Network Monitor Visualizzatore eventi.

Per altre informazioni sulla creazione di un ERP, vedere:

-   [Creazione di pagine di riferimento per gli eventi expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Scrittura di una pagina di riferimento eventi](writing-an-event-reference-page.md)
-   [Assegnazione di un nome a una pagina di riferimento eventi](naming-an-event-reference-page.md)

 

 



