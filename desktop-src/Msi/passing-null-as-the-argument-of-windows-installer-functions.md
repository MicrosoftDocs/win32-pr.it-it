---
description: 'Windows Installer funzioni che restituiscono dati in un utente specificato: la posizione di memoria non deve essere chiamata con null come valore per il puntatore.'
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Passaggio di valori null alle funzioni Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309467"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="500a3-103">Passaggio di null come argomento delle funzioni Windows Installer</span><span class="sxs-lookup"><span data-stu-id="500a3-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="500a3-104">Windows Installer funzioni che restituiscono dati in un utente specificato: la posizione di memoria non deve essere chiamata con null come valore per il puntatore.</span><span class="sxs-lookup"><span data-stu-id="500a3-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="500a3-105">Queste funzioni restituiscono una stringa o restituiscono dati come puntatori Integer, ma restituiscono valori incoerenti quando si passa null come valore per l'argomento di output.</span><span class="sxs-lookup"><span data-stu-id="500a3-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="500a3-106">Non passare null come valore dell'argomento output per una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="500a3-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="500a3-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="500a3-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="500a3-108">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="500a3-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="500a3-109">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="500a3-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="500a3-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="500a3-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="500a3-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="500a3-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="500a3-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="500a3-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="500a3-113">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="500a3-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="500a3-114">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="500a3-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="500a3-115">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="500a3-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="500a3-116">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="500a3-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="500a3-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="500a3-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="500a3-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="500a3-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="500a3-119">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="500a3-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="500a3-120">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="500a3-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



