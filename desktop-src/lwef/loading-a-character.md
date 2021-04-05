---
title: Caricamento di un carattere
description: Caricamento di un carattere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710378"
---
# <a name="loading-a-character"></a><span data-ttu-id="279b1-103">Caricamento di un carattere</span><span class="sxs-lookup"><span data-stu-id="279b1-103">Loading a Character</span></span>

<span data-ttu-id="279b1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="279b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="279b1-105">Per animare un carattere, è necessario innanzitutto caricare il carattere.</span><span class="sxs-lookup"><span data-stu-id="279b1-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="279b1-106">Utilizzare il metodo [**Load**](load-method.md) per caricare i dati del carattere.</span><span class="sxs-lookup"><span data-stu-id="279b1-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="279b1-107">Microsoft Agent supporta due formati per i dati di tipo carattere e animazione: un singolo file strutturato e file separati.</span><span class="sxs-lookup"><span data-stu-id="279b1-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="279b1-108">In genere, si usa il formato di file singolo (. ACS) quando i dati vengono archiviati localmente.</span><span class="sxs-lookup"><span data-stu-id="279b1-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="279b1-109">Il formato del file multiplo (. ACF,. ACA) funziona meglio quando si desidera scaricare animazioni singolarmente, ad esempio quando si accede alle animazioni da un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="279b1-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="279b1-110">Un'applicazione client può caricare una sola istanza dello stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="279b1-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="279b1-111">Qualsiasi tentativo di caricare lo stesso carattere più di una volta avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="279b1-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="279b1-112">Tuttavia, un'applicazione può disporre di più istanze dello stesso carattere caricate fornendo connessioni separate a Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="279b1-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="279b1-113">Ad esempio, un'applicazione potrebbe caricare lo stesso carattere da due copie del controllo Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="279b1-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="279b1-114">È anche possibile definire i propri caratteri da usare con Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="279b1-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="279b1-115">È possibile utilizzare qualsiasi strumento di rendering che si preferisce creare le immagini, purché si disponga di file in formato bitmap di Windows.</span><span class="sxs-lookup"><span data-stu-id="279b1-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="279b1-116">Per assemblare e compilare immagini di un carattere in animazioni da usare con Microsoft Agent, usare l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="279b1-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="279b1-117">Questo strumento consente di definire le proprietà predefinite di un carattere, nonché di definire animazioni per il carattere.</span><span class="sxs-lookup"><span data-stu-id="279b1-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="279b1-118">L'editor dei caratteri di Microsoft Agent consente inoltre di selezionare il formato di file appropriato quando si crea un carattere.</span><span class="sxs-lookup"><span data-stu-id="279b1-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




