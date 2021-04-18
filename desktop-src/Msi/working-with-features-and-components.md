---
description: Sono disponibili diverse funzioni che modificano l'installazione dei componenti e delle funzionalità del prodotto. Di seguito viene descritto come modificare le funzionalità e i componenti di.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Utilizzo delle funzionalità e dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313778"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="f7c91-104">Utilizzo delle funzionalità e dei componenti</span><span class="sxs-lookup"><span data-stu-id="f7c91-104">Working with Features and Components</span></span>

<span data-ttu-id="f7c91-105">Sono disponibili diverse funzioni che modificano l'installazione dei [componenti e delle funzionalità](components-and-features.md)del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7c91-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="f7c91-106">Di seguito viene descritto come modificare le funzionalità e i componenti di.</span><span class="sxs-lookup"><span data-stu-id="f7c91-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="f7c91-107">**Per modificare l'installazione di funzionalità e componenti**</span><span class="sxs-lookup"><span data-stu-id="f7c91-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="f7c91-108">Impostare il livello di installazione per un componente o una funzionalità chiamando la funzione [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="f7c91-109">A ogni funzionalità di un pacchetto viene assegnato un livello di installazione nella [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f7c91-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="f7c91-110">Se il livello di installazione di una funzionalità è inferiore al livello impostato da [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la funzionalità viene selezionata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f7c91-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="f7c91-111">Dopo la chiamata di **MsiSetInstallLevel** , è possibile modificare in modo esplicito se una funzionalità è installata.</span><span class="sxs-lookup"><span data-stu-id="f7c91-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="f7c91-112">Determinare gli stati disponibili per una funzionalità specificata chiamando la funzione [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="f7c91-113">Ottenere i requisiti di spazio su disco per una funzionalità specificata e le relative caratteristiche figlio chiamando la funzione [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="f7c91-114">Ottenere lo stato corrente di una funzionalità o di un componente chiamando la funzione [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="f7c91-115">Modificare lo stato della funzionalità o del componente con la funzione [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



