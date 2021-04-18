---
description: Questa sezione descrive le interfacce IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfacce di gestione metodi di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312862"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="7ea62-103">Interfacce di gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="7ea62-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="7ea62-104">Questa sezione descrive le interfacce IMM.</span><span class="sxs-lookup"><span data-stu-id="7ea62-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="7ea62-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="7ea62-105">Interface</span></span>                                                            | <span data-ttu-id="7ea62-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ea62-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ea62-107">**IFECommon**</span><span class="sxs-lookup"><span data-stu-id="7ea62-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="7ea62-108">Fornisce servizi correlati a IME comuni per linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="7ea62-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="7ea62-109">**IFEDictionary**</span><span class="sxs-lookup"><span data-stu-id="7ea62-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="7ea62-110">Consente ai client di accedere a un dizionario utenti Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="7ea62-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="7ea62-111">**IFELanguage**</span><span class="sxs-lookup"><span data-stu-id="7ea62-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="7ea62-112">Fornisce servizi di elaborazione del linguaggio utilizzando Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="7ea62-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="7ea62-113">**IImePad**</span><span class="sxs-lookup"><span data-stu-id="7ea62-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="7ea62-114">Inserisce il testo nelle app da IMEPadApplets che implementano l'interfaccia [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="7ea62-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="7ea62-115">**IImePadApplet**</span><span class="sxs-lookup"><span data-stu-id="7ea62-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="7ea62-116">Inserisce le stringhe nelle app tramite l'interfaccia [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .</span><span class="sxs-lookup"><span data-stu-id="7ea62-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="7ea62-117">**IImePlugInDictDictionaryList**</span><span class="sxs-lookup"><span data-stu-id="7ea62-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="7ea62-118">Consente di accedere all'elenco dei dizionari plug-in IME.</span><span class="sxs-lookup"><span data-stu-id="7ea62-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="7ea62-119">**IImeSpecifyApplets**</span><span class="sxs-lookup"><span data-stu-id="7ea62-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="7ea62-120">Specifica i metodi chiamati dall'oggetto interfaccia [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) per emulare l'interfaccia [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="7ea62-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



