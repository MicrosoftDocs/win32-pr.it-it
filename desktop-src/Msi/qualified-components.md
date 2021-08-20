---
description: Un componente completo è un metodo di riferimento indiretto a livello singolo, simile a un puntatore.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componenti qualificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c9a5ccd757516402a951afa3a105d51e3a0b3d22a88614983997dbcd6d07f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376304"
---
# <a name="qualified-components"></a>Componenti qualificati

Un componente completo è un metodo di riferimento indiretto a livello singolo, simile a un puntatore. I componenti qualificati vengono usati principalmente per raggruppare i componenti con funzionalità parallele in categorie. Ad esempio, se nella tabella [Componente](component-table.md) sono elencati 30 componenti che sono lo stesso modello di fax Microsoft Word localizzato in 30 lingue, è possibile raggrupparli in una categoria di componenti qualificati usando la tabella [PublishComponent](publishcomponent-table.md).

I componenti qualificati vengono immessi nella tabella Componente allo stesso modo dei componenti ordinari. Ogni componente deve avere un GUID ID componente univoco e un identificatore componente specificati nella tabella Componente. Inoltre, i componenti qualificati sono associati a un GUID di categoria e a un qualificatore di stringa di testo nella tabella PublishComponent. I componenti qualificati fanno riferimento al GUID della categoria e al qualificatore, che punta solo al componente normale nella tabella Component.

Ad esempio, un GUID di ID componente completo può puntare a versioni linguistiche diverse di una DLL di risorse. In questo caso, il gruppo di DLL di risorse localizzate comprende la categoria e le stringhe degli identificatori delle impostazioni locali numerici (LCID) vengono comunemente usate come qualificatori. Uno sviluppatore può creare un pacchetto di installazione che usa questi componenti qualificati per eseguire le operazioni seguenti:

-   Trovare il percorso di una determinata versione linguistica della DLL della risorsa [**usando MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e installare la risorsa.
-   Determinare tutte le versioni linguistiche della DLL di risorse presenti chiamando [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Preparare l'applicazione per supportare lingue aggiuntive. Una versione language pack per l'applicazione può usare il componente completo per aggiungere altre versioni linguistiche della DLL della risorsa.

Per altre informazioni, vedere [Uso di componenti qualificati.](using-qualified-components.md)

 

 



