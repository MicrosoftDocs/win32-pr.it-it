---
description: Un dispositivo Direct3D può trovarsi in uno stato operativo o in uno stato perso.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Dispositivi persi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341831"
---
# <a name="lost-devices-direct3d-9"></a>Dispositivi persi (Direct3D 9)

Un dispositivo Direct3D può trovarsi in uno stato operativo o in uno stato perso. Lo stato operativo è lo stato normale del dispositivo in cui viene eseguito il dispositivo e presenta tutti i rendering come previsto. Il dispositivo esegue una transizione allo stato perduto quando un evento, ad esempio la perdita dello stato attivo della tastiera in un'applicazione a schermo intero, causa l'impossibilità del rendering. Lo stato perso è caratterizzato dall'esito negativo di tutte le operazioni di rendering, il che significa che i metodi di rendering possono restituire codici di esito positivo anche se le operazioni di rendering hanno esito negativo. In questa situazione, il codice di errore D3DERR \_ DEVICELOST viene restituito da [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Per impostazione predefinita, non è stato specificato il set completo di scenari che possono causare la perdita di un dispositivo. Alcuni esempi tipici includono la perdita dello stato attivo, ad esempio quando l'utente preme ALT + TAB o quando viene inizializzata una finestra di dialogo di sistema. I dispositivi possono anche essere persi a causa di un evento di risparmio energia o quando un'altra applicazione presuppone un'operazione a schermo intero. Inoltre, qualsiasi errore di [**IDirect3DDevice9:: Reset imposta**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) lo stato di smarrimento del dispositivo.

Tutti i metodi che derivano da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) possono funzionare dopo la perdita di un dispositivo. Dopo la perdita del dispositivo, ogni funzione ha in genere le tre opzioni seguenti:

-   Errore con D3DERR \_ DEVICELOST: ciò significa che l'applicazione deve riconoscere che il dispositivo è andato perso, in modo che l'applicazione identifichi che qualcosa non si sta verificando come previsto.
-   Fail in modo invisibile all'utente, restituendo S \_ OK o qualsiasi altro codice restituito: se una funzione ha esito negativo in modo invisibile all'utente, l'applicazione in genere non può distinguere il risultato di "success" e un "errore invisibile all'utente".
-   La funzione restituisce un codice restituito.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Un dispositivo Direct3D 9 restituisce D3DERR \_ DEVICELOST. Una volta che è stata restituita da [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), il comportamento di emulazione non funziona più e tutte le chiamate future avranno esito negativo fino a quando il dispositivo non viene reimpostato correttamente.<br/> Un dispositivo Direct3D 9Ex non restituisce mai D3DERR \_ DEVICELOST, ma può restituire nuovi messaggi di stato (vedere [modifiche del comportamento del dispositivo](dx9lh.md)).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Risposta a un dispositivo perso

Un dispositivo perso deve ricreare le risorse, incluse le risorse di memoria video, dopo la reimpostazione. Se un dispositivo viene perso, l'applicazione esegue una query sul dispositivo per verificare se può essere ripristinato allo stato operativo. In caso contrario, l'applicazione attende fino a quando il dispositivo non può essere ripristinato.

Se il dispositivo può essere ripristinato, l'applicazione prepara il dispositivo distruggendo tutte le risorse di memoria video ed eventuali catene di scambio. Quindi, l'applicazione chiama il metodo [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Reset è l'unico metodo che ha effetto in caso di perdita di un dispositivo ed è l'unico metodo con cui un'applicazione può modificare il dispositivo da un perso a uno stato operativo. Il ripristino avrà esito negativo a meno che l'applicazione non rilasci tutte le risorse allocate in D3DPOOL \_ default, incluse quelle create dai metodi [**IDirect3DDevice9:: CreateRenderTarget**](/windows/desktop/api) e [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Nella maggior parte dei casi, le chiamate ad alta frequenza di Direct3D non restituiscono informazioni sull'eventuale perdita del dispositivo. L'applicazione può continuare a chiamare metodi di rendering, ad esempio [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), senza ricevere una notifica di un dispositivo perso. Internamente, queste operazioni vengono scartate fino a quando il dispositivo non viene reimpostato sullo stato operativo.

L'applicazione può determinare le operazioni da eseguire in caso di perdita di un dispositivo, eseguendo una query sul valore restituito del metodo [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) .

## <a name="locking-operations"></a>Operazioni di blocco

Internamente, Direct3D funziona a sufficienza per garantire che un'operazione di blocco venga completata dopo la perdita di un dispositivo. Tuttavia, non è garantito che i dati della risorsa di memoria video saranno accurati durante l'operazione di blocco. Si garantisce che non verrà restituito alcun codice di errore. In questo modo, le applicazioni possono essere scritte senza preoccuparsi della perdita del dispositivo durante un'operazione di blocco.

## <a name="resources"></a>Risorse

Le risorse possono utilizzare la memoria video. Poiché un dispositivo smarrito è disconnesso dalla memoria video di proprietà dell'adapter, non è possibile garantire l'allocazione della memoria video quando il dispositivo viene perso. Di conseguenza, tutti i metodi di creazione delle risorse vengono implementati per avere esito positivo restituendo D3D \_ OK, ma in realtà allocano solo la memoria di sistema fittizia. Poiché le risorse di memoria video devono essere distrutte prima del ridimensionamento del dispositivo, non si verificano problemi di allocazione eccessiva della memoria del video. Queste superfici fittizie consentono di visualizzare le operazioni di blocco e di copia in modo che funzionino normalmente finché l'applicazione non chiama [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reinviate e rileva che il dispositivo è andato perso.

Per poter reimpostare un dispositivo da uno stato perso a uno stato operativo, è necessario rilasciare tutta la memoria del video. Ciò significa che l'applicazione deve rilasciare le catene di scambio create con [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e tutte le risorse inserite nella \_ classe di memoria predefinita D3DPOOL. L'applicazione non deve rilasciare le risorse nelle \_ classi di Memoria D3DPOOL gestite o D3DPOOL \_ SYSTEMMEM. Altri dati di stato vengono eliminati automaticamente dalla transizione a uno stato operativo.

Si consiglia di sviluppare applicazioni con un unico percorso di codice per rispondere alla perdita del dispositivo. Questo percorso di codice è probabilmente simile, se non identico, al percorso del codice eseguito per inizializzare il dispositivo all'avvio.

## <a name="retrieved-data"></a>Dati recuperati

Direct3D consente alle applicazioni di convalidare gli Stati di trama e di rendering rispetto al rendering single-pass da parte dell'hardware usando [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Questo metodo, che viene in genere richiamato durante l'inizializzazione dell'applicazione, restituirà D3DERR \_ DEVICELOST se il dispositivo è andato perso.

Direct3D consente inoltre alle applicazioni di copiare immagini generate o scritte in precedenza da risorse di memoria video a risorse di memoria di sistema non volatili. Poiché le immagini di origine di tali trasferimenti potrebbero andare perse in qualsiasi momento, Direct3D consente di eseguire tali operazioni di copia quando il dispositivo viene perso.

Per quanto riguarda le query asincrone, [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce D3DERR \_ DEVICELOST se viene specificato il flag di svuotamento, per indicare all'applicazione che **IDirect3DQuery9:: GetData** non restituirà mai S \_ OK.

L'operazione di copia, [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api), può avere esito negativo con D3DERR \_ DEVICELOST poiché non è presente alcuna superficie primaria quando il dispositivo viene perso. [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) può anche avere esito negativo con D3DERR \_ DEVICELOST perché non è possibile creare un buffer nascosto quando il dispositivo viene perso. Si noti che questi casi sono l'unica istanza di D3DERR \_ DEVICELOST al di fuori dei metodi [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)reinviate, [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)e [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) .

## <a name="programmable-shaders"></a>Shader programmabili

In Direct3D 9, i vertex shader e i pixel shader non devono essere ricreati dopo la reimpostazione. Verranno memorizzate. Nelle versioni precedenti di DirectX, un dispositivo perso richiedeva la ricreazione degli shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
