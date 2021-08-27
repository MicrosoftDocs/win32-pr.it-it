---
description: Livelli API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Livelli API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd452032eda61c49edbf007b5ebaf0314f9054fe0b016cf07e3f4473ae3abee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119991"
---
# <a name="api-layers-direct3d-10"></a>Livelli API (Direct3D 10)

Il runtime Direct3D 10 è costruito con livelli, a partire dalle funzionalità di base alla base e creando funzionalità facoltative e assistete dallo sviluppatore nei livelli esterni.

## <a name="core-layer"></a>Livello principale

Il livello principale esiste per impostazione predefinita. fornendo un mapping molto sottile tra l'API e il driver di dispositivo, riducendo al minimo il sovraccarico per le chiamate ad alta frequenza. Poiché il livello principale è essenziale per le prestazioni, esegue solo la convalida critica.

I livelli rimanenti sono facoltativi. Come regola generale, i livelli aggiungono funzionalità, ma non modificano il comportamento esistente. Ad esempio, le funzioni di base avranno gli stessi valori restituiti indipendentemente dal livello di debug di cui viene creata un'istanza, anche se è possibile fornire un output di debug aggiuntivo se viene creata un'istanza del livello di debug.

Creare livelli quando viene creato un dispositivo chiamando [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) e fornendo uno o più [**valori D3D10 \_ CREATE DEVICE \_ \_ FLAG.**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)

## <a name="debug-layer"></a>Livello di debug

Il livello di debug offre una convalida estesa dei parametri aggiuntivi e della coerenza, ad esempio la convalida del collegamento dello shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione di descrizioni degli errori. L'output generato dal livello di debug è costituito da una coda di stringhe accessibili tramite l'interfaccia [**ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (vedere Personalizzare l'output di debug [con ID3D10InfoQueue (Direct3D 10).](d3d10-graphics-programming-guide-api-features-layers-info-queue.md) Gli errori generati dal livello principale vengono evidenziati con avvisi dal livello di debug.

Per creare un dispositivo che supporta il livello di debug, è necessario installare DirectX SDK (per ottenere D3D10SDKLayers.DLL) e quindi specificare il flag D3D10 CREATE DEVICE DEBUG quando si \_ \_ chiama \_ [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). Naturalmente, l'esecuzione di un'applicazione con il livello di debug sarà notevolmente più lenta. Per abilitare o disabilitare i messaggi di debug per le API D3DX10, chiamare [**D3DX10DebugMute**](d3dx10debugmute.md).

Quando il livello di debug elenca le perdite di memoria, restituisce un elenco di puntatori a interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza &gt; nome ". È possibile impostare il nome descrittivo usando il [**metodo ID3D10DeviceChild::SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) e il GUID **WKPDID \_ D3DDebugObjectName** presente in D3Dcommon.h. Ad esempio, per assegnare a pTexture il nome SDKLayer mytexture.jpg, usare il codice seguente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In genere, è consigliabile compilare queste chiamate dalla versione di produzione.

## <a name="switch-to-reference-layer"></a>Passaggio al livello di riferimento

Questo livello consente a un'applicazione di eseguire la transizione tra un dispositivo hardware (HAL) e un dispositivo di riferimento o software (REF). Per cambiare dispositivo, è necessario prima creare un dispositivo che supporti il livello switch-to-reference (vedere [**D3D10CreateDevice)**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)e quindi chiamare [**ID3D10SwitchToRef::SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Tutti gli stati, le risorse e gli oggetti del dispositivo vengono mantenuti tramite questa transizione del dispositivo. Tuttavia, a volte non è possibile trovare corrispondenze esatte con i dati delle risorse. Ciò è dovuto al fatto che alcune informazioni sono disponibili per un dispositivo hardware che non è disponibile per un dispositivo di riferimento.

Praticamente tutte le applicazioni in tempo reale usano l'implementazione HAL della pipeline. Quando la pipeline passa da un dispositivo hardware a un dispositivo di riferimento, le operazioni di rendering vengono eseguite simultaneamente sia nell'hardware che nel software. Durante il rendering del dispositivo software, sarà necessario scaricare le risorse nella memoria di sistema. Ciò potrebbe richiedere la sgombero di altre risorse memorizzate nella cache di sistema per fare spazio.

> [!Note]  
> Questa funzionalità switch-to-reference-layer è supportata solo in Direct3D 10 e Direct3D 10.1 e non è più supportata in Direct3D 11 e versioni successive.

 

## <a name="thread-safe-layer"></a>Thread-Safe livello

Questo livello è progettato per consentire alle applicazioni multithread di accedere al dispositivo da più thread.

Un'applicazione Direct3D 10 può controllare la sincronizzazione di un dispositivo usando le funzioni del dispositivo. Ciò consente a un'applicazione di abilitare/disabilitare le sezioni critiche (abilitando o disabilitando temporaneamente la protezione multithreading) e di attivare/rilasciare un blocco di sezione critica su più punti di ingresso dell'API Direct3D 10. Il livello thread-safe è abilitato per impostazione predefinita. Per le applicazioni a thread singolo, il livello thread-safe non ha alcun impatto sulle prestazioni.




Differenze tra Direct3D 9 e Direct3D 10:

- A differenza di Direct3D 9, per impostazione predefinita l'API Direct3D 10 è completamente thread-safe.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




