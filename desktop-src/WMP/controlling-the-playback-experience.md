---
title: Controllo dell'esperienza di riproduzione
description: Controllo dell'esperienza di riproduzione
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows playlist di metafile multimediali, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Windows playlist di metafile multimediali, problemi di riproduzione
- playlist, problemi di riproduzione
- playlist di metafile, problemi di riproduzione
- controllo della riproduzione
- Windows Media Player,controllo della riproduzione
- Windows Media Player, problemi di riproduzione
- HTMLView, problemi di riproduzione
- HTMLView, controllo della riproduzione
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341888"
---
# <a name="controlling-the-playback-experience"></a>Controllo dell'esperienza di riproduzione

Questa sezione illustra alcuni dei problemi di riproduzione che possono verificarsi quando si usa la funzionalità HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Richiedere all'utente di visualizzare il contenuto basato sul Web

È possibile decidere che si vuole che gli utenti possano usufruire del contenuto multimediale digitale solo quando viene visualizzato anche il contenuto basato sul Web HTMLView. È possibile includere codice script nella pagina Web HTMLView che arresta la riproduzione del contenuto multimediale digitale se l'utente si allontana dalla **funzionalità In** riproduzione. A tale scopo, è possibile specificare un gestore eventi per l'evento **unload** come parte dell'elemento **BODY,** come illustrato nel codice HTML seguente:


```XML
<BODY onunload = "UnloadMe();">

```



È quindi possibile includere il codice script nella funzione del gestore eventi per chiudere il file nel lettore. Il codice di esempio seguente esegue questa operazione:


```XML
function UnloadMe()
{
   Player.close();
}

```



Quando l'utente  passa da Ora in riproduzione facendo clic su un pulsante per aprire un'altra funzionalità Windows Media Player, ad esempio la libreria, Il lettore chiude il browser incorporato. In questo modo si **verifica l'evento onunload,** eseguendo lo script nella funzione **denominata UnloadMe**. Il [metodo Player.close](player-close.md) arresta la riproduzione e scarica il file multimediale digitale corrente. Per visualizzare di nuovo il contenuto, l'utente deve riaprire il file asx originale. Questa tecnica arresta anche la riproduzione quando l'utente si allontana dalla pagina Web HTMLView. Si noti che questa tecnica non può impedire all'utente di visualizzare il contenuto multimediale digitale quando passa alla modalità interfaccia.

Si ricorderà che il parametro HTMLView può essere applicato a ogni **elemento ENTRY** in un file asx. È possibile sfruttare questa funzionalità per assicurarsi che il contenuto HTMLView sia visualizzato ogni volta che viene avviato un nuovo file multimediale digitale. A tale scopo, associare un **elemento PARAM** per HTMLView a ogni voce nella playlist asx. Quando ogni voce viene riprodotta, il lettore torna alla modalità completa e visualizza il contenuto HTMLView specificato nella playlist.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>I tipi di comando di script URL e FILE sono disabilitati per impostazione predefinita

Windows Media Player serie 9 o successive fornisce impostazioni che consentono all'utente di specificare se i comandi script di tipo URL e FILE possono essere eseguiti. Per impostazione predefinita, entrambi questi tipi di comando script non vengono eseguiti. Se si usano tipi di comandi script personalizzati, continueranno a essere eseguiti, indipendentemente dall'impostazione dell'utente. Se è necessario usare i comandi di script URL e FILE, è necessario richiedere all'utente di modificare le impostazioni. Per modificare le impostazioni, fare **clic su Strumenti**, quindi su **Opzioni** e infine **su Sicurezza**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>La riapertura di un controllo HTMLView non ricarica la pagina Web

Quando l'utente apre un file asx che include un parametro HTMLView e successivamente riapre lo stesso file, Windows Media Player non aggiorna la pagina Web HTMLView. Ciò significa anche che se è stato consentito agli utenti di spostarsi dalla pagina Web HTMLView, Player non restituisce il browser incorporato alla pagina Web HTMLView iniziale.

## <a name="hiding-the-content-location"></a>Nascondere il percorso del contenuto

È possibile decidere di non voler Windows Media Player il percorso del contenuto multimediale digitale durante la riproduzione di un file asx. In genere, Windows Media Player solo informazioni sulla playlist stessa quando si esegue lo streaming di contenuto da Internet. Tuttavia, è possibile eseguire altri passaggi per impedire agli utenti di determinare la posizione del contenuto. Ad esempio, un modo per assicurarsi che Player non visualizza il percorso del contenuto è trasmettere il contenuto usando Servizi Windows Media playlist sul lato server. In questo modo, quando l'utente visualizza le proprietà per il contenuto, vede l'URL del server e non l'URL del contenuto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




