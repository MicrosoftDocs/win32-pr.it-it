---
description: Per eseguire correttamente un'applicazione, è necessario che nel computer host siano installate le DLL appropriate. Queste dll possono essere fornite dal sistema operativo o dal pacchetto ridistribuibile delle applicazioni.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Collegamento di librerie statiche e dinamiche (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304716"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Collegamento di librerie statiche e dinamiche (Direct3D 10)

Per eseguire correttamente un'applicazione, è necessario che nel computer host siano installate le DLL appropriate. Queste dll possono essere fornite dal sistema operativo o dal pacchetto ridistribuibile delle applicazioni.

## <a name="libraries-load-appropriate-dlls"></a>Librerie che caricano le DLL appropriate

Le librerie incluse in DirectX SDK caricherà automaticamente le DLL appropriate in fase di esecuzione. L'eccezione a questa regola è d3dx10. lib/d3dx10d. lib, che caricherà il d3dx10.dll fornito con la versione dell'SDK. Se, ad esempio, l'SDK scaricato include d3dx10 \_33.dll e d3dx10 \_34.dll, la libreria (d3dx10. lib) fornita con tale SDK caricherà d3dx10 \_34.dll. Se successivamente viene installato un SDK successivo contenente d3dx10 \_ 35. lib, d3dx10. lib dell'SDK precedente caricherà comunque d3dx10 \_34.dll. D3dx10. lib dell'SDK più recente caricherà d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Ridistribuzione di file binari

È possibile ridistribuire solo d3dx10.dll e versioni successive dello stesso file. Per ridistribuire il file, è necessario utilizzare la funzione **DirectXSetup** . Per informazioni dettagliate sull'uso di questa funzione e sulla combinazione di un pacchetto ridistribuibile, vedere [installazione di DirectX con DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx). Tutti gli altri file binari necessari sono inclusi in Windows Vista. Gli unici file binari che è possibile ridistribuire sono quelli presenti nella directory seguente.


```
(SDK root)\Redist
```



La tabella seguente descrive i binari che gli sviluppatori devono conoscere.



| File binari Direct3D 10   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Componenti D3DX10 per la vendita al dettaglio e di debug; i componenti per la vendita al dettaglio possono essere ridistribuiti nel file CAB REDIST.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Rasterizzazione riferimenti. Fornisce l'implementazione del software della pipeline grafica. Inclusa solo come parte del Windows SDK o di DirectX SDK legacy e non può essere ridistribuita. L'rasterizzazione dei riferimenti è destinato solo al debug. Il collegamento esplicito non è necessario. il tentativo di creare un dispositivo di riferimento (vedere [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) caricherà questa dll se è presente.                                                                                                    |
| d3d10sdklayers.dll     | Serie di utilità SDK che fungono da livello tra le chiamate API e l'esecuzione del runtime, inclusi il [livello di debug](d3d10-graphics-programming-guide-api-features-layers.md) e il livello di commutazione a riferimento. Il collegamento esplicito non è necessario. Se viene creato un dispositivo con il flag di livello appropriato, questa DLL viene caricata automaticamente. Questo componente è progettato solo a scopo di sviluppo e debug. Inclusa solo come parte del Windows SDK o di DirectX SDK legacy e non può essere ridistribuita. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Grafica Direct3D 10](d3d10-graphics.md)
</dt> </dl>

 

 



