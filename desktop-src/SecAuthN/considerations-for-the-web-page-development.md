---
description: Il broker di autenticazione Web si basa sulle stesse tecnologie di Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considerazioni relative allo sviluppo di pagine Web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346006"
---
# <a name="considerations-for-the-web-page-development"></a>Considerazioni relative allo sviluppo di pagine Web

Il broker di autenticazione Web si basa sulle stesse tecnologie di Internet Explorer in Windows. Tuttavia, a causa di uno scopo speciale di questo componente alcune funzionalità di Internet Explorer sono state disabilitate o bloccate a una configurazione specifica. Inoltre, il broker di autenticazione Web fornisce un canale di registrazione eventi dedicato per facilitare la risoluzione dei problemi relativi alle pagine elaborate.

## <a name="internet-explorer-10-standard-document-mode"></a>Modalità documento standard di Internet Explorer 10

Il broker di autenticazione Web Visualizza tutte le pagine in "modalità standard IE10". È possibile utilizzare gli strumenti di sviluppo di Internet Explorer per vedere il funzionamento della pagina in modalità documento diverse. Per ulteriori informazioni sulla compatibilità con Internet Explorer 10, vedere gli argomenti MSDN per [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Funzionalità disabilitate e bloccate

Diverse funzionalità di Internet Explorer sono completamente disabilitate o bloccate in base a valori specifici che non possono essere modificati nelle opzioni Internet del sistema operativo.



| Funzionalità                            | Stato                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API della cache dell'applicazione ("AppCache") | Disabled                                                                                                                                                                                                        |
| Cronologia collegamenti                       | Disabled                                                                                                                                                                                                        |
| File temporanei                    | Abilitato                                                                                                                                                                                                         |
| Cookie                            | I cookie di sessione sono abilitati. I cookie salvati in modo permanente sono consentiti, ma sono soggetti a pulizia automatica, a meno che il broker di autenticazione Web non sia in modalità SSO. Per ulteriori informazioni, vedere la sezione Single Sign-on. |
| DATABASE di indice                           | Disabled                                                                                                                                                                                                        |
| Archiviazione DOM                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Download di file                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Requisito HTTPS

Il primo URL che un'applicazione userà per comunicare con il provider online deve essere HTTPS.

## <a name="dimension-for-different-window-sizes"></a>Dimensione per diverse dimensioni della finestra

Un'app di Windows 8 può essere visualizzata in diverse dimensioni, ad esempio a schermo intero, a una finestra ridimensionata o all'interno di un fascino, ad esempio l'accesso alla condivisione. A seconda del layout della finestra in cui viene visualizzato il broker di autenticazione Web, le dimensioni con cui le pagine Web devono funzionare potrebbero essere diverse. Per ulteriori informazioni, vedere l'argomento [linee guida per il ridimensionamento in layout ristretti](/previous-versions/windows/hh465371(v=win.10)) e le [linee guida per la condivisione del contenuto](/previous-versions/windows/hh465251(v=win.10)) .

La pagina Web deve usare le query per supporti CSS per verificare le dimensioni necessarie per l'uso e il lay-out di conseguenza. La pagina, tuttavia, non deve essere progettata in base ai pixel esatti documentati in questo articolo e deve essere in grado di ridimensionare le diverse dimensioni. Le dimensioni specificate in questo documento sono soggette a modifiche nelle versioni future del sistema operativo.

Se una pagina non può contenere tutte le informazioni nello spazio assegnato, ad esempio un lungo elenco di autorizzazioni richieste da un'applicazione, il broker di autenticazione Web fornirà barre di scorrimento per consentire all'utente di scorrere la pagina in base alle esigenze. Lo zoom è fornito anche da Pinch zoom per i dispositivi basati su tocco e CTRL + rotellina del mouse per PC desktop e portatili.

Per testare diversi fattori di scalabilità, usare l' [app di esempio Web Authentication broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) caricata in Microsoft Visual Studio Professional 2012, che consente di simulare lo schermo intero e gli stati ridimensionati.

Oltre ai diversi layout documentati in precedenza, assicurarsi di testare la pagina in modo diverso, ad esempio verticale e orizzontale, con diverse impostazioni locali e lingue, nonché con funzionalità di accessibilità come l'opzione "Rendi tutto più grande" attivata.

I layout disponibili sono:

-   [Schermo intero](#full-screen)
-   [Finestra ridimensionata](#resized)
-   [Visualizzazione Charm](#charm-view)
-   [Visualizzazione selezione file](#file-picker-view)

### <a name="full-screen"></a>Schermo intero

Per il layout a schermo intero, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Height: altezza dello schermo (dipende dalla risoluzione dello schermo)

Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nel layout a schermo intero.

![esempio di interfaccia utente di broker di autenticazione Web nel layout a schermo intero](images/wab-figure2.png)

### <a name="resized"></a>Ridimensionata

Per una finestra ridimensionata, le dimensioni della pagina Web possono essere:

-   Larghezza: 260 pixel
-   Height: altezza dello schermo (dipende dalla risoluzione dello schermo)

Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web in una finestra ridimensionata nella pagina Web XBox. Si noti che l'interfaccia utente di broker di autenticazione Web si trova solo sul lato destro dell'acquisizione dello schermo.

![esempio di interfaccia utente di broker di autenticazione Web in una finestra ridimensionata](images/wab-figure3.png)

### <a name="charm-view"></a>Visualizzazione Charm

Per la visualizzazione Charm, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Height: altezza dello schermo (dipende dalla risoluzione dello schermo)

Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nella visualizzazione Charm.

![un esempio mostra l'interfaccia utente di broker di autenticazione Web nella visualizzazione Charm](images/wab-figure4.png)

### <a name="file-picker-view"></a>Visualizzazione selezione file

Per la visualizzazione selezione file, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Height: altezza dello schermo (dipende dalla risoluzione dello schermo)

Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nella visualizzazione di selezione file.

![un esempio mostra l'interfaccia utente di broker di autenticazione Web nella visualizzazione selezione file](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Nessuna nuova finestra per impostazione predefinita

Per impostazione predefinita, nessun URL provocherà l'apertura di una nuova finestra, ma verrà invece visualizzata nella finestra gestore di autenticazione Web. Questo include il metodo JavaScript Window. Open, l'attributo "target" dei collegamenti ipertestuali oppure quando l'utente usa il meccanismo CTRL + clic per forzare l'apertura di una nuova finestra. L'eccezione a questa regola si verifica quando una pagina Web dichiara un collegamento come sicuro per spostarsi in un browser, come descritto nella pagina relativa alla personalizzazione della destinazione dei collegamenti ipertestuali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
