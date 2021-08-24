---
description: Web Authentication Broker si basa sulle stesse tecnologie che si basano Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considerazioni relative allo sviluppo di pagine Web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22932f40d5268059fc30e97817de0b3671cee7447974b038ea4be12eedd76ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883278"
---
# <a name="considerations-for-the-web-page-development"></a>Considerazioni relative allo sviluppo di pagine Web

Web Authentication Broker si basa sulle stesse tecnologie che si basano Internet Explorer in Windows. Tuttavia, a causa di uno scopo molto speciale di questo componente, alcune funzionalità del Internet Explorer sono state disabilitate o bloccate a una configurazione specifica. Il Gestore autenticazione Web fornisce anche un canale di registrazione eventi dedicato per la risoluzione dei problemi relativi alle pagine che elabora.

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10 documento standard

Il Gestore autenticazione Web visualizza tutte le pagine in "Modalità standard IE10". È possibile usare gli strumenti di sviluppo in Internet Explorer per vedere il funzionamento della pagina in modalità documento diverse. Per altre informazioni sulla compatibilità Internet Explorer 10, vedere gli argomenti MSDN per [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Funzionalità disabilitate e bloccate

Diverse funzionalità di Internet Explorer sono completamente disabilitate o bloccate su valori specifici che non possono essere modificati in Opzioni Internet del sistema operativo.



| Funzionalità                            | Stato                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API cache dell'applicazione ("AppCache") | Disabled                                                                                                                                                                                                        |
| Cronologia dei collegamenti                       | Disabled                                                                                                                                                                                                        |
| File temporanei                    | Attivato                                                                                                                                                                                                         |
| Cookie                            | I cookie di sessione sono abilitati. I cookie persistenti sono consentiti, ma sono soggetti alla pulizia automatica a meno che Web Authentication Broker non sia in modalità SSO. Per altre informazioni, vedere la sezione Single Sign-On. |
| Index DB                           | Disabled                                                                                                                                                                                                        |
| Archiviazione DOM                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Download di file                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Requisito HTTPS

Il primo URL che un'applicazione userà per comunicare con il provider online deve essere HTTPS.

## <a name="dimension-for-different-window-sizes"></a>Dimensione per dimensioni di finestra diverse

Un Windows 8 app può essere visualizzata in diverse dimensioni, ad esempio schermo intero, finestra ridimensionata o all'interno di un accesso, ad esempio Condividi accesso. A seconda del layout della finestra visualizzato da Web Authentication Broker, le dimensioni con cui devono funzionare le pagine Web potrebbero essere diverse. Per altre informazioni, vedere [l'argomento Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) (Linee guida per il ridimensionamento per limitare i layout) e [Guidelines for sharing content (Linee guida per la condivisione di contenuto).](/previous-versions/windows/hh465251(v=win.10))

La pagina Web deve usare le query di supporto CSS per verificare le dimensioni con cui deve funzionare e disponersi di conseguenza. Tuttavia, la pagina non deve essere progettata in base ai pixel esatti documentati qui e deve essere in grado di ridimensionarsi a dimensioni diverse. Le dimensioni specificate in questo documento sono soggette a modifiche nelle versioni future del sistema operativo.

Se una pagina non può contenere tutte le informazioni nello spazio assegnato (ad esempio, un lungo elenco di autorizzazioni richieste da un'applicazione), Il Gestore autenticazione Web fornirà barre di scorrimento per consentire all'utente di scorrere la pagina in base alle esigenze. Lo zoom è disponibile anche avvicinando le dita per i dispositivi basati sul tocco e premendo CTRL+rotellina del mouse per PC desktop e portatili.

Per testare diversi fattori di ridimensionamento, usare l'app di esempio [Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) caricata in Microsoft Visual Studio Professional 2012, che consente di simulare lo schermo intero e gli stati ridimensionati.

Oltre ai diversi layout documentati in precedenza, assicurarsi di testare la pagina con un orientamento dello schermo diverso (ad esempio verticale e orizzontale), impostazioni locali e lingue diverse, nonché con funzionalità di accessibilità come l'opzione "Aumenta le dimensioni" attivata.

I layout disponibili sono:

-   [Schermo intero](#full-screen)
-   [Finestra ridimensionata](#resized)
-   [Visualizzazione Accessi](#charm-view)
-   [Visualizzazione selezione file](#file-picker-view)

### <a name="full-screen"></a>Schermo intero

Per il layout a schermo intero, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Altezza: altezza dello schermo (dipende dalla risoluzione dello schermo)

L'esempio seguente mostra l'interfaccia utente del broker di autenticazione Web nel layout a schermo intero.

![un esempio di interfaccia utente del broker di autenticazione Web nel layout a schermo intero](images/wab-figure2.png)

### <a name="resized"></a>Ridimensionato

Per una finestra ridimensionata, le dimensioni della pagina Web possono essere:

-   Larghezza: 260 pixel
-   Altezza: altezza dello schermo (dipende dalla risoluzione dello schermo)

L'esempio seguente mostra l'interfaccia utente di Web Authentication Broker in una finestra ridimensionata nella pagina Web XBox. Si noti che l'interfaccia utente di Web Authentication Broker si trova solo sul lato destro della schermata.

![esempio di interfaccia utente del broker di autenticazione Web in una finestra ridimensionata](images/wab-figure3.png)

### <a name="charm-view"></a>Visualizzazione Accessi

Per la visualizzazione Accessi, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Altezza: altezza dello schermo (dipende dalla risoluzione dello schermo)

L'esempio seguente mostra l'interfaccia utente di Web Authentication Broker nella visualizzazione Accessi.

![un esempio mostra l'interfaccia utente del broker di autenticazione Web nella visualizzazione accessi](images/wab-figure4.png)

### <a name="file-picker-view"></a>Visualizzazione selezione file

Per la visualizzazione selezione file, le dimensioni della pagina Web sono:

-   Larghezza: 566 pixel
-   Altezza: altezza dello schermo (dipende dalla risoluzione dello schermo)

L'esempio seguente mostra l'interfaccia utente di Web Authentication Broker nella visualizzazione selezione file.

![un esempio mostra l'interfaccia utente del broker di autenticazione Web nella visualizzazione selezione file](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Nessuna nuova finestra per impostazione predefinita

Per impostazione predefinita, nessun URL comporta l'apertura di una nuova finestra, ma verrà invece visualizzato all'interno della finestra Gestore autenticazione Web. Sono inclusi il metodo JavaScript window.open, l'attributo "target" dei collegamenti ipertestuali o quando l'utente usa il meccanismo CTRL+clic per forzare l'apertura di una nuova finestra. L'eccezione a questa regola si verifica quando una pagina Web dichiara un collegamento come sicuro da esplorare in un browser, come descritto in Personalizzazione della destinazione dei collegamenti ipertestuali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[App di esempio Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
