---
title: Personalizzare l'anteprima di un'icona e una bitmap di anteprima in tempo reale
description: Mostra come personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale (denominata anche anteprima di anteprima).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323874"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Personalizzare l'anteprima di un'icona e una bitmap di anteprima in tempo reale

## <a name="description"></a>Descrizione

È possibile personalizzare un'anteprima iconica e una bitmap in *tempo reale* (o *Anteprima*) utilizzando le funzioni e i messaggi introdotti nelle api di Windows 7 Gestione finestre desktop (DWM).

In particolare, è possibile usare la funzione [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) e il messaggio [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) per personalizzare un'anteprima iconica. È anche possibile usare la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) e il messaggio [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) per impostare una bitmap di anteprima dinamica iconica.

Per un'applicazione di esempio che usa la funzione **DwmSetIconicThumbnail** , vedere [esempio di TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

Nella figura seguente viene illustrata un'anteprima predefinita trasformata in un'anteprima personalizzata.

![illustrazione di un'immagine di anteprima originale e di un'immagine di anteprima modificata con una bitmap personalizzata](images/customthumbnail.jpg)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista                          |
| Server minimo supportato | Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008 |
| Windows SDK minimo      | [Windows Software Development Kit (SDK) per Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Compilazione dell'esempio TabThumbnails

**Per compilare l'esempio utilizzando Microsoft Visual Studio (metodo preferito)**

1.  Aprire Esplora risorse e passare alla cartella in cui si trova il file TabThumbnails. sln.
2.  Fare doppio clic sul file di soluzione (con estensione sln) per aprire il file in Microsoft Visual Studio.
3.  Nel menu **Compila** scegliere **Compila soluzione**. L'applicazione viene compilata nella \\ directory di debug o di \\ versione predefinita.

**Per compilare l'esempio utilizzando il prompt dei comandi**

1.  Aprire una finestra del prompt dei comandi e passare alla directory di esempio.
2.  Immettere `msbuild TabThumbnails.sln`.

## <a name="related-topics"></a>Argomenti correlati

[Gestione finestre desktop](dwm-overview.md)

[Sviluppo per Windows](/windows/desktop/win32-and-com-development)
