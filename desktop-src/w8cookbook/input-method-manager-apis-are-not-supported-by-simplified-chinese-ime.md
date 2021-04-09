---
title: Le API di input Method Manager non sono supportate dall'IME cinese semplificato
description: Le API di input Method Manager non sono supportate dall'IME cinese semplificato
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118011"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="d7a09-103">Le API di input Method Manager non sono supportate dall'IME cinese semplificato</span><span class="sxs-lookup"><span data-stu-id="d7a09-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="d7a09-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="d7a09-104">Platforms</span></span>

<dl> <span data-ttu-id="d7a09-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d7a09-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="d7a09-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d7a09-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="d7a09-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7a09-107">Description</span></span>

<span data-ttu-id="d7a09-108">Le seguenti API del gestore del metodo di input non sono supportate dagli IME cinese semplificato in Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="d7a09-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="d7a09-109">Interfaccia IFECommon</span><span class="sxs-lookup"><span data-stu-id="d7a09-109">IFECommon interface</span></span>
-   <span data-ttu-id="d7a09-110">Interfaccia IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="d7a09-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="d7a09-111">Interfaccia IFELanguage</span><span class="sxs-lookup"><span data-stu-id="d7a09-111">IFELanguage interface</span></span>
-   <span data-ttu-id="d7a09-112">Interfaccia IImePad</span><span class="sxs-lookup"><span data-stu-id="d7a09-112">IImePad interface</span></span>
-   <span data-ttu-id="d7a09-113">Interfaccia IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="d7a09-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="d7a09-114">Interfaccia IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="d7a09-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="d7a09-115">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="d7a09-115">Manifestations</span></span>

<span data-ttu-id="d7a09-116">Le funzioni che usano tali API non funzionano con l'IME cinese semplificato.</span><span class="sxs-lookup"><span data-stu-id="d7a09-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="d7a09-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="d7a09-117">Solution</span></span>

<span data-ttu-id="d7a09-118">Le applicazioni devono essere progettate in modo che gli utenti possano completare l'attività desiderata senza usare l'API specificata.</span><span class="sxs-lookup"><span data-stu-id="d7a09-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="d7a09-119">Risorse</span><span class="sxs-lookup"><span data-stu-id="d7a09-119">Resources</span></span>

-   [<span data-ttu-id="d7a09-120">Interfacce di gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="d7a09-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="d7a09-121">IFECommon</span><span class="sxs-lookup"><span data-stu-id="d7a09-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="d7a09-122">Interfaccia IFECommon</span><span class="sxs-lookup"><span data-stu-id="d7a09-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="d7a09-123">Interfaccia IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="d7a09-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="d7a09-124">IFELanguage</span><span class="sxs-lookup"><span data-stu-id="d7a09-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="d7a09-125">IImePad</span><span class="sxs-lookup"><span data-stu-id="d7a09-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="d7a09-126">IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="d7a09-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="d7a09-127">IimePlugInDictDictionaryList</span><span class="sxs-lookup"><span data-stu-id="d7a09-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="d7a09-128">IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="d7a09-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 