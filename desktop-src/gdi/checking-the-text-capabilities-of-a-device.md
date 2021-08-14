---
description: È possibile usare le funzioni EnumFonts ed EnumFontFamilies per enumerare i tipi di carattere disponibili in un contesto di dispositivo di memoria compatibile con la stampante.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Controllo delle funzionalità di testo di un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7121e7b5e2a416d06d79dba33c9a7c2eb7f6fb26d766a30b383f024e87e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354851"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Controllo delle funzionalità di testo di un dispositivo

È possibile usare le [funzioni EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) ed [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) per enumerare i tipi di carattere disponibili in un contesto di dispositivo di memoria compatibile con la stampante. È anche possibile usare la [funzione GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare informazioni sulle funzionalità di testo di un dispositivo. Chiamando la [**funzione GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) con l'indice NUMFONTS, è possibile determinare il numero minimo di tipi di carattere supportati da una stampante. Una singola stampante può supportare più tipi di carattere di quelli specificati nel valore restituito da **GetDeviceCaps** con l'indice NUMFONTS. Usando l'indice TEXTCAPS, è possibile identificare molte delle funzionalità di testo del dispositivo specificato.

 

 
