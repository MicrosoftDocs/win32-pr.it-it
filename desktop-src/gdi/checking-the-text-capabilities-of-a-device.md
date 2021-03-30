---
description: È possibile utilizzare le funzioni EnumFonts e EnumFontFamilies per enumerare i tipi di carattere disponibili in un contesto di dispositivo di memoria compatibile con la stampante.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Verifica delle funzionalità di testo di un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994101"
---
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="25661-103">Verifica delle funzionalità di testo di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="25661-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="25661-104">È possibile utilizzare le funzioni [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) per enumerare i tipi di carattere disponibili in un contesto di dispositivo di memoria compatibile con la stampante.</span><span class="sxs-lookup"><span data-stu-id="25661-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="25661-105">È anche possibile usare la funzione [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare informazioni sulle funzionalità di testo di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25661-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="25661-106">Chiamando la funzione [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) con l'indice NUMFONTS, è possibile determinare il numero minimo di tipi di carattere supportati da una stampante.</span><span class="sxs-lookup"><span data-stu-id="25661-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="25661-107">Una singola stampante può supportare più tipi di carattere rispetto a quelli specificati nel valore restituito da **GetDeviceCaps** con l'indice NUMFONTS. Usando l'indice TEXTCAPS è possibile identificare molte delle funzionalità di testo del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="25661-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
