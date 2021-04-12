---
description: Il programma di installazione può aumentare la resilienza dell'applicazione reinstallando automaticamente i componenti danneggiati.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Ricerca di una funzionalità o di un componente danneggiato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232065"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="f868c-103">Ricerca di una funzionalità o di un componente danneggiato</span><span class="sxs-lookup"><span data-stu-id="f868c-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="f868c-104">Il programma di installazione può aumentare la [resilienza](resiliency.md) dell'applicazione reinstallando automaticamente i componenti danneggiati.</span><span class="sxs-lookup"><span data-stu-id="f868c-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="f868c-105">In particolare, il programma di installazione Reinstalla un componente o una funzionalità se rileva che il file o la chiave del registro di sistema specificata nella colonna percorso chiave della [tabella dei componenti](component-table.md) è mancante.</span><span class="sxs-lookup"><span data-stu-id="f868c-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="f868c-106">Se il percorso di tasto del componente di una funzionalità è danneggiato nell'origine o se si verifica un errore nel modo in cui viene creato il tasto di scelta rapida nel database, il programma di installazione può tentare di aprire un pacchetto di installazione e reinstallare la funzionalità ogni volta che viene attivato il collegamento della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f868c-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="f868c-107">Per determinare la provocazione di tentativi ripetuti di reinstallare una funzionalità o un'applicazione, controllare nel registro eventi la presenza di due voci come la seguente.</span><span class="sxs-lookup"><span data-stu-id="f868c-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="f868c-108">Il primo messaggio indica quale componente del pacchetto del prodotto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="f868c-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="f868c-109">Si tratta del componente a cui si fa riferimento nella \_ colonna componente della [tabella dei collegamenti](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="f868c-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="f868c-110">Il secondo messaggio indica quale componente non riesce a rilevare.</span><span class="sxs-lookup"><span data-stu-id="f868c-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="f868c-111">Si tratta del componente con il percorso della finestra di avvio della reinstallazione mancante o danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f868c-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



