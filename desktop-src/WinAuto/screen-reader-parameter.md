---
title: Parametro Visualizzatore schermo
description: Il parametro screen reader indica se un'applicazione deve fornire informazioni testuali in situazioni in cui in caso contrario le informazioni verranno presentate graficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047016"
---
# <a name="screen-reader-parameter"></a><span data-ttu-id="068af-103">Parametro Visualizzatore schermo</span><span class="sxs-lookup"><span data-stu-id="068af-103">Screen reader parameter</span></span>

<span data-ttu-id="068af-104">Il parametro screen reader indica se un'applicazione deve fornire informazioni testuali in situazioni in cui in caso contrario le informazioni verranno presentate graficamente.</span><span class="sxs-lookup"><span data-stu-id="068af-104">The screen reader parameter indicates whether an application should provide textual information in situations where it would otherwise present the information graphically.</span></span>

<span data-ttu-id="068af-105">Questo parametro viene in genere impostato da strumenti di accessibilità, ad esempio utilità per la lettura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="068af-105">This parameter is typically set by accessibility aids such as screen readers.</span></span> <span data-ttu-id="068af-106">Le applicazioni usano i flag **SPI \_ GETSCREENREADER** e **SPI \_ SETSCREENREADER** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di lettura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="068af-106">Applications use the **SPI\_GETSCREENREADER** and **SPI\_SETSCREENREADER** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the screen reader parameter.</span></span>

> [!Note]  
> <span data-ttu-id="068af-107">Assistente vocale, lo screen reader incluso in Windows, non imposta i flag **SPI \_ SETSCREENREADER** o **SPI \_ GETSCREENREADER**</span><span class="sxs-lookup"><span data-stu-id="068af-107">Narrator, the screen reader that is included with Windows, does not set the **SPI\_SETSCREENREADER** or **SPI\_GETSCREENREADER** flags.</span></span>

 

 

 