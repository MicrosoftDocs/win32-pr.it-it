---
description: Viene illustrato come scrivere un gestore utilizzato per visualizzare un'anteprima del file nel riquadro di anteprima di Esplora risorse o in altri host del gestore di anteprime.
title: Esempio di gestore anteprima file recipe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980247"
---
# <a name="recipe-preview-handler-sample"></a>Esempio di gestore anteprima file recipe

Viene illustrato come scrivere un gestore utilizzato per visualizzare un'anteprima del file nel riquadro di anteprima di Esplora risorse o in altri host del gestore di anteprime.

In questo argomento sono incluse le sezioni seguenti:

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Annullamento della registrazione della DLL del gestore di anteprime di esempio](#unregistering-the-sample-preview-handler-dll)
-   [Argomenti correlati](#related-topics)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio RecipePreviewHandler](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **RecipePreviewHandler** . Ad esempio: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Immettere `msbuild PreviewHandlerSDKSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **RecipePreviewHandler** .
2.  Fare doppio clic sull'icona per il file PreviewHandlerSDKSample. sln per aprire il progetto in Visual Studio.
    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila soluzione** dal menu **Compila** .

> [!Note]  
> Se il sistema di destinazione è a 64 bit (x64), questo gestore di anteprime di esempio deve essere compilato come applicazione a 64 bit.

 

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **RecipePreviewHandler** compilata. Ad esempio: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Immettere `regsvr32.exe PreviewHandlerSDKSample.dll` per registrare il gestore.
2.  Aprire Esplora risorse e visualizzare il riquadro di anteprima se non è già visualizzato.
    -   **Windows 7**: fare clic sul pulsante anteprima del riquadro.
    -   **Windows Vista**: fare clic sul menu **organizza** , passare al sottomenu **layout** e selezionare **riquadro di anteprima**.
3.  Utilizzare Esplora risorse per passare alla directory del progetto **RecipePreviewHandler** .
4.  Selezionare il file example. recipe.

Per fare in modo che l'output a 32 bit (x86) e 64 bit (x64) funzioni in una versione di Windows a 64 bit, impostare il valore **AppID** sull'host surrogato WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , come illustrato nel codice seguente.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Annullamento della registrazione della DLL del gestore di anteprime di esempio

-   Aprire la finestra del prompt dei comandi e immettere `regsvr32.exe /u PreviewHandlerSDKSample.dll` per annullare la registrazione del gestore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
