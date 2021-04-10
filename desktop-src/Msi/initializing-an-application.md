---
description: Per abilitare la funzionalità del programma di installazione, un'applicazione deve chiamare una serie di funzioni durante l'inizializzazione.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inizializzazione di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227191"
---
# <a name="initializing-an-application"></a><span data-ttu-id="7f35d-103">Inizializzazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7f35d-103">Initializing an Application</span></span>

<span data-ttu-id="7f35d-104">Per abilitare la funzionalità del programma di installazione, un'applicazione deve chiamare una serie di funzioni durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="7f35d-105">Per ulteriori informazioni, vedere [meccanismo di installazione](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="7f35d-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="7f35d-106">Nei passaggi seguenti viene descritto come utilizzare il programma di installazione per inizializzare un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="7f35d-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="7f35d-107">**Per inizializzare un'applicazione**</span><span class="sxs-lookup"><span data-stu-id="7f35d-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="7f35d-108">Chiamare la funzione [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) in modo che l'applicazione possa identificare se stessa nel programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="7f35d-109">Il codice prodotto è un parametro obbligatorio per molte funzioni del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="7f35d-110">Chiamare la funzione [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) per raccogliere le informazioni utente alla prima avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="7f35d-111">Se la chiamata a [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) ha esito negativo, chiamare la funzione [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) per raccogliere informazioni sull'utente.</span><span class="sxs-lookup"><span data-stu-id="7f35d-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="7f35d-112">Se necessario, visualizzare un'interfaccia utente predefinita chiamando la funzione [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .</span><span class="sxs-lookup"><span data-stu-id="7f35d-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="7f35d-113">Per creare un'interfaccia utente personalizzata, registrarla con il programma di installazione chiamando la funzione [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="7f35d-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="7f35d-114">Chiamare la funzione [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) per impostare il livello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="7f35d-115">Presentare all'utente le funzionalità disponibili enumerando le funzionalità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="7f35d-116">È possibile enumerare le funzionalità nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f35d-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="7f35d-117">Eseguire una query sul programma di installazione funzionalità per funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7f35d-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="7f35d-118">Ad esempio, prima che l'applicazione disegni un pulsante o una voce di menu, l'applicazione chiama la funzione [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) in modo che il programma di installazione possa verificare che la funzionalità sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f35d-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="7f35d-119">Enumerare tutte le funzionalità disponibili contemporaneamente chiamando la funzione [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) .</span><span class="sxs-lookup"><span data-stu-id="7f35d-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="7f35d-120">Per usare questa funzione, l'applicazione deve chiamare ripetutamente **MsiEnumFeatures** durante l'incremento di un indice.</span><span class="sxs-lookup"><span data-stu-id="7f35d-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="7f35d-121">Ottenere informazioni dettagliate sull'installazione corrente chiamando le funzioni di enumerazione seguenti ripetutamente, incrementando una variabile di indice per ogni chiamata:</span><span class="sxs-lookup"><span data-stu-id="7f35d-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="7f35d-122">Chiamare la funzione [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) per enumerare i prodotti registrati con il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="7f35d-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="7f35d-123">Chiamare la funzione [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) per enumerare i componenti.</span><span class="sxs-lookup"><span data-stu-id="7f35d-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="7f35d-124">Chiamare la funzione [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) per enumerare i qualificatori di componente.</span><span class="sxs-lookup"><span data-stu-id="7f35d-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="7f35d-125">Chiamare la funzione [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) per enumerare i prodotti per un componente specifico.</span><span class="sxs-lookup"><span data-stu-id="7f35d-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="7f35d-126">Se il valore restituito in una funzione di enumerazione è \_ esito positivo errore, sono ancora presenti altri elementi da enumerare e la funzione deve essere chiamata nuovamente con una variabile di indice incrementata.</span><span class="sxs-lookup"><span data-stu-id="7f35d-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="7f35d-127">Se il valore restituito è errore \_ , non sono presenti \_ altri \_ elementi, tutti gli elementi sono stati enumerati e la funzione non deve essere chiamata nuovamente.</span><span class="sxs-lookup"><span data-stu-id="7f35d-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



