---
description: Creazione di una pagina delle proprietà del filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Creazione di una pagina delle proprietà del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303972"
---
# <a name="creating-a-filter-property-page"></a>Creazione di una pagina delle proprietà del filtro

Questa sezione descrive come creare una pagina delle proprietà per un filtro DirectShow personalizzato, usando la classe [**CBasePropertyPage**](cbasepropertypage.md) . Il codice di esempio riportato in questa sezione illustra tutti i passaggi necessari per creare una pagina delle proprietà. Nell'esempio viene illustrata una pagina delle proprietà per un filtro effetto video ipotetico che supporta una proprietà saturazione. La pagina delle proprietà dispone di un dispositivo di scorrimento, che può essere spostato dall'utente per regolare il livello di saturazione del filtro.

Questa sezione contiene i seguenti argomenti:

-   [Passaggio 1. Definire un meccanismo per l'impostazione della proprietà](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Passaggio 2. Implementare ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Passaggio 3. Supporta QueryInterface](step-3--support-queryinterface.md)
-   [Passaggio 4. Creazione della pagina delle proprietà](step-4--create-the-property-page.md)
-   [Passaggio 5. Archiviare un puntatore al filtro](step-5--store-a-pointer-to-the-filter.md)
-   [Passaggio 6. Inizializzare la finestra di dialogo](step-6--initialize-the-dialog.md)
-   [Passaggio 7. Gestire i messaggi della finestra](step-7--handle-window-messages.md)
-   [Passaggio 8. Applicare le modifiche alle proprietà](step-8--apply-property-changes.md)
-   [Passaggio 9. Disconnettere la pagina delle proprietà](step-9--disconnect-the-property-page.md)
-   [Passaggio 10. Supporto della registrazione COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



