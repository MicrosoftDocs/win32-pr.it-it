---
description: Livelli API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Livelli API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427083bdcaf389c4b01b590a1bc3fef7eb878b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401396"
---
# <a name="api-layers-direct3d-10"></a>Livelli API (Direct3D 10)

Il runtime di Direct3D 10 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni.

## <a name="core-layer"></a>Livello principale

Il livello principale esiste per impostazione predefinita. fornire un mapping molto sottile tra l'API e il driver di dispositivo, riducendo al minimo l'overhead per le chiamate ad alta frequenza. Poiché il livello principale è essenziale per le prestazioni, viene eseguita solo la convalida critica.

I livelli rimanenti sono facoltativi. Come regola generale, i livelli aggiungono funzionalità, ma non modificano il comportamento esistente. Le funzioni di base, ad esempio, avranno gli stessi valori restituiti indipendentemente dal livello di debug di cui viene creata un'istanza, sebbene sia possibile fornire un output di debug aggiuntivo se viene creata un'istanza del livello debug.

Creare livelli quando un dispositivo viene creato chiamando [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) e specificando uno o più valori [**di \_ \_ \_ flag di creazione del dispositivo d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) .

## <a name="debug-layer"></a>Livello di debug

Il livello di debug fornisce la convalida estesa di parametri e coerenza, ad esempio la convalida del collegamento shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione delle descrizioni degli errori. L'output generato dal livello di debug è costituito da una coda di stringhe accessibili tramite l' [**interfaccia ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (vedere [personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Gli errori generati dal livello di base sono evidenziati con avvisi dal livello di debug.

Per creare un dispositivo che supporta il livello di debug, è necessario installare DirectX SDK (per ottenere D3D10SDKLayers.DLL), quindi specificare il flag di debug per la creazione di un \_ dispositivo d3d10 \_ quando si \_ chiama [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). Naturalmente, l'esecuzione di un'applicazione con il livello di debug sarà sostanzialmente più lenta. Per abilitare o disabilitare i messaggi di debug per le API D3DX10, chiamare [**D3DX10DebugMute**](d3dx10debugmute.md).

Quando il livello di debug elenca le perdite di memoria, viene restituito un elenco di puntatori dell'interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza nome &gt; ". È possibile impostare il nome descrittivo usando il metodo [**ID3D10DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) e il GUID **WKPDID \_ D3DDebugObjectName** in D3Dcommon. h. Ad esempio, per assegnare un nome a pTexture con il nome SDKLayer mytexture.jpg, usare il codice seguente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In genere, è necessario compilare queste chiamate fuori dalla versione di produzione.

## <a name="switch-to-reference-layer"></a>Livello passaggio a riferimento

Questo livello consente a un'applicazione di eseguire la transizione tra un dispositivo hardware (HAL) e un riferimento o un dispositivo software (REF). Per passare a un dispositivo, è prima necessario creare un dispositivo che supporta il livello di commutazione a riferimento (vedere [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) e quindi chiamare [**ID3D10SwitchToRef:: SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Tutti gli Stati dei dispositivi, le risorse e gli oggetti vengono mantenuti tramite questa transizione del dispositivo. Tuttavia, talvolta non è possibile trovare esattamente una corrispondenza con i dati delle risorse. Ciò è dovuto al fatto che alcune informazioni sono disponibili per un dispositivo hardware che non è disponibile per un dispositivo di riferimento.

Quasi tutte le applicazioni in tempo reale usano l'implementazione HAL della pipeline. Quando la pipeline passa da un dispositivo hardware a un dispositivo di riferimento, le operazioni di rendering vengono eseguite contemporaneamente sia nell'hardware che nel software. Con il rendering del dispositivo software, sarà necessario scaricare le risorse nella memoria di sistema. Questa operazione potrebbe richiedere la rimozione di altre risorse memorizzate nella cache di sistema per fare spazio.

> [!Note]  
> Questa funzionalità di livello switch-to-Reference è supportata solo in Direct3D 10 e Direct3D 10,1 e non è più supportata in Direct3D 11 e versioni successive.

 

## <a name="thread-safe-layer"></a>Livello Thread-Safe

Questo livello è progettato per consentire alle applicazioni multithread di accedere al dispositivo da più thread.

Un'applicazione Direct3D 10 può controllare la sincronizzazione di un dispositivo usando le funzioni del dispositivo. Questo consente a un'applicazione di abilitare/disabilitare le sezioni critiche (abilitazione/disabilitazione temporanea della protezione multithreading) e di prendere/rilasciare un blocco di sezione critica su più punti di ingresso dell'API Direct3D 10. Il livello thread-safe è abilitato per impostazione predefinita. Per le applicazioni a thread singolo, il livello thread-safe non ha alcun effetto sulle prestazioni.



|                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> A differenza di Direct3D 9, l'impostazione predefinita dell'API Direct3D 10 è completamente thread-safe.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




