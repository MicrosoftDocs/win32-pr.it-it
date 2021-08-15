---
description: Illustra come controllare il comportamento di raggruppamento della barra delle applicazioni delle finestre di un'applicazione tramite la System.AppUserModel.ID proprietà .
title: Esempio di proprietà delle finestre ID modello utente applicazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a6a4b0daca8b6bd4147c1e36d921b58b3802d975e678e49a9b9153761e61820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219881"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Esempio di proprietà della finestra Application User Model ID (AppID)

Illustra come controllare il comportamento di raggruppamento della barra delle applicazioni delle finestre di un'applicazione tramite la [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) proprietà .

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra come impostare la [proprietà System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) tramite l'uso dell'implementazione [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) della finestra, ottenuta tramite [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto AppUserModelIDWindowProperty.**
2.  Immettere `msbuild AppUserModelIDWindowProperty.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory del **progetto AppUserModelIDWindowProperty.**
2.  Fare doppio clic sull'icona per il file AppUserModelIDWindowProperty.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `AppUserModelIDWindowProperty.exe` . In alternativa, da esplora Windows fare doppio clic sull'icona per AppUserModelIDWindowProperty.exe.
3.  Per dimostrare l'effetto degli ID modello utente dell'applicazione (AppUserModelID) sul raggruppamento della barra delle applicazioni, avviare contemporaneamente almeno tre istanze dell'applicazione.
4.  Usare il menu per impostare un AppUserModelID diverso in ognuna delle tre finestre. Si noti che ogni AppUserModelID separato comporta un pulsante della barra delle applicazioni separato e che le finestre possono modificare la propria identità in fase di esecuzione.
5.  Impostare almeno due finestre sul secondo AppUserModelID. Si noti che entrambi si spostano nello stesso gruppo della barra delle applicazioni.
6.  Aprire la finestra **Proprietà della barra delle applicazioni** e del menu Start facendo clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliendo **Proprietà** nel menu di scelta rapida. Modificare i pulsanti **della barra delle applicazioni:** nell'elenco a discesa Combina quando la barra delle applicazioni **è piena** e Non combinare **mai i** valori. Si noti che ogni finestra può ottenere un pulsante separato, ma che i pulsanti sono raggruppati in base a AppUserModelID.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
