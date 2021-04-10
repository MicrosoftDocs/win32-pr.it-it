---
description: Sono disponibili diverse funzioni che devono essere chiamate da un'applicazione per la richiesta di funzionalità.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Richiesta di una funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050252"
---
# <a name="requesting-a-feature"></a><span data-ttu-id="0407c-103">Richiesta di una funzionalità</span><span class="sxs-lookup"><span data-stu-id="0407c-103">Requesting a Feature</span></span>

<span data-ttu-id="0407c-104">Sono disponibili diverse funzioni che devono essere chiamate da un'applicazione per la richiesta di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0407c-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="0407c-105">Prima di richiedere una funzionalità, l'applicazione deve verificare che la funzionalità sia installata.</span><span class="sxs-lookup"><span data-stu-id="0407c-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="0407c-106">Se l'applicazione chiama [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) prima che l'applicazione acceda a una funzionalità, l'applicazione può usare le informazioni restituite per mantenere le metriche di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="0407c-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="0407c-107">**Per richiedere una funzionalità**</span><span class="sxs-lookup"><span data-stu-id="0407c-107">**To request a feature**</span></span>

1.  <span data-ttu-id="0407c-108">Chiamare la funzione [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se si desidera determinare la disponibilità di una funzionalità senza incrementare il numero di utilizzi.</span><span class="sxs-lookup"><span data-stu-id="0407c-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="0407c-109">Indicare la finalità dell'applicazione di usare una funzionalità chiamando la funzione [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="0407c-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="0407c-110">Determinare i percorsi dei file chiamando la funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .</span><span class="sxs-lookup"><span data-stu-id="0407c-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="0407c-111">Configurare la funzionalità chiamando la funzione [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="0407c-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="0407c-112">Ottenere le metriche di utilizzo che l'applicazione può usare chiamando la funzione [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .</span><span class="sxs-lookup"><span data-stu-id="0407c-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="0407c-113">Il diagramma seguente illustra il modello di richiesta di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0407c-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="0407c-114">modello di richiesta di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0407c-114">feature request model.</span></span> ](images/over2.png)

 

 



