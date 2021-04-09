---
description: Un componente completo è un metodo di riferimento indiretto a livello singolo, simile a un puntatore.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componenti qualificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881490"
---
# <a name="qualified-components"></a>Componenti qualificati

Un componente completo è un metodo di riferimento indiretto a livello singolo, simile a un puntatore. I componenti qualificati vengono utilizzati principalmente per raggruppare i componenti con funzionalità parallele in categorie. Se, ad esempio, nella [tabella](component-table.md) dei componenti sono elencati 30 componenti che corrispondono al modello Fax di Microsoft Word localizzato in 30 lingue, è possibile raggrupparli in una categoria di componenti qualificati utilizzando la [tabella PublishComponent](publishcomponent-table.md).

I componenti qualificati vengono immessi nella tabella dei componenti in modo analogo ai componenti normali. Ogni componente deve avere un GUID ID componente univoco e un identificatore componente specificato nella tabella dei componenti. Inoltre, i componenti qualificati sono associati a un GUID di categoria e a un qualificatore di stringa di testo nella tabella PublishComponent. Ai componenti qualificati viene fatto riferimento dal GUID della categoria e dal qualificatore, che punta solo al componente ordinario nella tabella dei componenti.

Ad esempio, un GUID ID componente qualificato può puntare a versioni diverse di una DLL di risorse. In questo caso, il gruppo di dll di risorse localizzate comprende la categoria e le stringhe di identificatori delle impostazioni locali (LCID) numerici vengono comunemente usate come qualificatori. Uno sviluppatore può creare un pacchetto di installazione che utilizza questi componenti qualificati per eseguire le operazioni seguenti:

-   Trovare il percorso di una particolare versione in lingua della DLL della risorsa usando [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e installare la risorsa.
-   Determinare tutte le versioni del linguaggio della DLL della risorsa presenti chiamando [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Preparare l'applicazione per il supporto di lingue aggiuntive. Un Language Pack futuro per l'applicazione può usare il componente qualificato per aggiungere altre versioni della lingua della DLL di risorse.

Per ulteriori informazioni, vedere [utilizzo di componenti qualificati](using-qualified-components.md).

 

 



