---
description: Aggiunta di nodi di output con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Aggiunta di nodi di output con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481977"
---
# <a name="adding-output-nodes-with-topoedit"></a>Aggiunta di nodi di output con TopoEdit

In una topologia un nodo di output rappresenta un sink multimediale che riceve i dati multimediali da un nodo di trasformazione e lo presenta per la riproduzione. Il tipo di nodo di output dipende dal tipo di supporto del nodo di origine.

Nella tabella seguente viene illustrato il comando menu/barra degli strumenti per l'aggiunta di un nodo di output alla topologia.




| Tipo di supporto di origine | Comando menu/barra degli strumenti | Descrizione | 
|-------------------|----------------------|-------------|
| Flusso audio | Scegliere <strong>Aggiungi</strong> SAR dal menu <strong>Topologia</strong>. | Crea un nodo di output per il renderer audio di streaming (SAR) che riproduce un flusso audio tramite un dispositivo audio, ad esempio una scheda audio. | 
| Flusso video | Scegliere <strong>Aggiungi</strong> <strong>EVR</strong>dal menu Topologia . | Crea un nodo di output per il renderer video avanzato (EVR) che visualizza i fotogrammi per un flusso video. | 
| Sink multimediale personalizzato | <ol><li>Scegliere <strong>Aggiungi</strong> sink personalizzato dal menu <strong>Topologia</strong>.<br /> Verrà <strong>visualizzata la finestra di dialogo INPUT GUID</strong> personalizzato .<br /></li><li><p>Nel <strong>campo GUID:</strong> immettere il GUID del sink personalizzato da aggiungere alla topologia.<br /></p><blockquote>[!Note]<br />TopoEdit prevede il GUID nel formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". In caso contrario, non riesce ad aggiungere il nodo e visualizza un messaggio di errore "GUID non valido".</blockquote><p><br /></p></li><li>Fare clic su <strong>OK</strong>.<br /></li></ol> | Crea un nodo di output per il sink di flusso per un'origine multimediale personalizzata.<br /> Il sink personalizzato deve supportare <strong>CoCreateInstance</strong> in modo che il sink possa essere specificato con un CLSID.<br /> | 




 

TopoEdit crea il nodo di output specificato. Il **riquadro Topologia mostra** il nodo di output come una casella verde che mostra il nome del sink di flusso.

Per informazioni sull'aggiunta di nodi di output a livello di codice Media Foundation API di output, vedere [Creazione di nodi di output](creating-output-nodes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 




