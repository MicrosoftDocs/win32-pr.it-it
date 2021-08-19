---
description: Un dispositivo Direct3D può essere in uno stato operativo o perso.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Dispositivi persi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038d03f1d95e4beb90d0e592fc666972db4e92e5a2a986a7711023a6b9fa05b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728579"
---
# <a name="lost-devices-direct3d-9"></a>Dispositivi persi (Direct3D 9)

Un dispositivo Direct3D può essere in uno stato operativo o perso. Lo stato operativo è lo stato normale del dispositivo in cui il dispositivo viene eseguito e presenta tutto il rendering come previsto. Il dispositivo esegue una transizione allo stato perso quando un evento, ad esempio la perdita dello stato attivo della tastiera in un'applicazione a schermo intero, rende impossibile il rendering. Lo stato perso è caratterizzato dall'errore invisibile all'utente di tutte le operazioni di rendering, il che significa che i metodi di rendering possono restituire codici di esito positivo anche se le operazioni di rendering hanno esito negativo. In questo caso, il codice di errore D3DERR DEVICELOST viene restituito da \_ [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Per impostazione predefinita, non viene specificato il set completo di scenari che possono causare la perdita di un dispositivo. Alcuni esempi tipici includono la perdita dello stato attivo, ad esempio quando l'utente preme ALT+TAB o quando viene inizializzata una finestra di dialogo di sistema. I dispositivi possono anche andare persi a causa di un evento di risparmio energia o quando un'altra applicazione presuppone un'operazione a schermo intero. Inoltre, qualsiasi errore da [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) porta il dispositivo in uno stato perso.

Tutti i metodi che derivano [**da IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) funzionano in modo garantito dopo la perdita di un dispositivo. Dopo la perdita del dispositivo, ogni funzione ha in genere le tre opzioni seguenti:

-   Fail with D3DERR DEVICELOST (Errore con D3DERR DEVICELOST) - Ciò significa che l'applicazione deve riconoscere che il dispositivo è stato perso, in modo che l'applicazione identifichi che qualcosa non accade \_ come previsto.
-   Errore invisibile all'utente, restituzione di S OK o di qualsiasi altro codice restituito: se una funzione ha esito negativo in modo invisibile all'utente, l'applicazione in genere non è in grado di distinguere tra il risultato di "esito positivo" e un "errore invisibile \_ all'utente".
-   La funzione restituisce un codice restituito.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Un dispositivo Direct3D 9 restituisce D3DERR \_ DEVICELOST. Dopo che è stato restituito da [**IDirect3DDevice9::P resent,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)il comportamento di emulazione non funziona più e tutte le chiamate future avranno esito negativo fino a quando il dispositivo non viene reimpostato correttamente.<br/> Un dispositivo Direct3D 9Ex non restituisce mai D3DERR DEVICELOST, ma può restituire nuovi messaggi di stato \_ (vedere Modifiche [del comportamento del dispositivo).](dx9lh.md)<br/> |



 

## <a name="responding-to-a-lost-device"></a>Risposta a un dispositivo perso

Un dispositivo perso deve creare nuovamente le risorse (incluse le risorse di memoria video) dopo che è stato reimpostato. Se un dispositivo viene perso, l'applicazione esegue una query sul dispositivo per verificare se può essere ripristinato allo stato operativo. In caso contrario, l'applicazione attende il ripristino del dispositivo.

Se il dispositivo può essere ripristinato, l'applicazione prepara il dispositivo distruendo tutte le risorse di memoria video ed eventuali catene di scambio. L'applicazione chiama quindi il [**metodo IDirect3DDevice9::Reset.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Reset è l'unico metodo che ha effetto quando un dispositivo viene perso ed è l'unico metodo con cui un'applicazione può modificare il dispositivo da uno stato perso a uno stato operativo. La reimpostazione avrà esito negativo a meno che l'applicazione non rilasci tutte le risorse allocate in D3DPOOL DEFAULT, incluse quelle create dai metodi \_ [**IDirect3DDevice9::CreateRenderTarget**](/windows/desktop/api) e [**IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

Nella maggior parte dei casi, le chiamate ad alta frequenza di Direct3D non restituiscono informazioni sulla perdita del dispositivo. L'applicazione può continuare a chiamare metodi di rendering, ad esempio [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)senza ricevere la notifica di un dispositivo perso. Internamente, queste operazioni vengono eliminate fino a quando il dispositivo non viene reimpostato sullo stato operativo.

L'applicazione può determinare cosa fare quando si verifica un dispositivo perso tramite una query sul valore restituito del metodo [**IDirect3DDevice9::TestCooperativeLevel.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)

## <a name="locking-operations"></a>Operazioni di blocco

Internamente, Direct3D esegue un lavoro sufficiente per garantire che un'operazione di blocco riesca dopo la perdita di un dispositivo. Tuttavia, non è garantito che i dati della risorsa di memoria video saranno accurati durante l'operazione di blocco. È garantito che non verrà restituito alcun codice di errore. In questo modo le applicazioni possono essere scritte senza alcun problema per la perdita del dispositivo durante un'operazione di blocco.

## <a name="resources"></a>Risorse

Le risorse possono utilizzare la memoria video. Poiché un dispositivo perso viene disconnesso dalla memoria video di proprietà dell'adattatore, non è possibile garantire l'allocazione della memoria video quando il dispositivo viene perso. Di conseguenza, tutti i metodi di creazione delle risorse vengono implementati per avere esito positivo con la restituzione di D3D OK, ma in realtà allocano solo \_ memoria di sistema fittizia. Poiché qualsiasi risorsa di memoria video deve essere distrutta prima del ridimensionamento del dispositivo, non si verifica alcun problema di sovraallocazione della memoria video. Queste superfici fittizie consentono il funzionamento normale delle operazioni di blocco e copia fino a quando l'applicazione non chiama [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) e rileva che il dispositivo è stato perso.

Tutta la memoria video deve essere rilasciata prima che un dispositivo possa essere reimpostato da uno stato perso a uno stato operativo. Ciò significa che l'applicazione deve rilasciare tutte le catene di scambio create con [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e tutte le risorse inserite nella classe di memoria D3DPOOL \_ DEFAULT. L'applicazione non deve rilasciare risorse nelle classi di memoria D3DPOOL MANAGED o \_ D3DPOOL \_ SYSTEMMEM. Altri dati sullo stato vengono automaticamente distrutti dalla transizione a uno stato operativo.

Si consiglia di sviluppare applicazioni con un unico percorso di codice per rispondere alla perdita di dispositivi. Questo percorso del codice è probabilmente simile, se non identico, al percorso del codice seguito per inizializzare il dispositivo all'avvio.

## <a name="retrieved-data"></a>Dati recuperati

Direct3D consente alle applicazioni di convalidare gli stati di trama ed eseguire il rendering rispetto al rendering a passaggio singolo da parte dell'hardware [**usando IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Questo metodo, che in genere viene richiamato durante l'inizializzazione dell'applicazione, restituirà D3DERR \_ DEVICELOST se il dispositivo è stato perso.

Direct3D consente inoltre alle applicazioni di copiare immagini generate o scritte in precedenza da risorse di memoria video a risorse di memoria di sistema non volatile. Poiché le immagini di origine di tali trasferimenti potrebbero andare perse in qualsiasi momento, Direct3D consente che tali operazioni di copia non riescano quando il dispositivo viene perso.

Per quanto riguarda le query asincrone, [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce D3DERR DEVICELOST se viene specificato il flag FLUSH, per indicare all'applicazione che \_ **IDirect3DQuery9::GetData** non restituirà mai S \_ OK.

L'operazione di [**copia, IDirect3DDevice9::GetFrontBufferData,**](/windows/desktop/api)può avere esito negativo con D3DERR DEVICELOST perché non esiste alcuna superficie primaria quando il dispositivo \_ viene perso. [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) può anche avere esito negativo con D3DERR DEVICELOST perché non è possibile creare un buffer nascosto quando il dispositivo \_ viene perso. Si noti che questi casi sono l'unica istanza di D3DERR DEVICELOST all'esterno dei metodi \_ [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), [**IDirect3DDevice9::TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)e [**IDirect3DDevice9::Reset.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)

## <a name="programmable-shaders"></a>Shader programmabili

In Direct3D 9 non è necessario creare nuovamente vertex shader e pixel shader dopo la reimpostazione. Verranno memorizzati. Nelle versioni precedenti di DirectX, un dispositivo perso richiedeva la creazione di shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
