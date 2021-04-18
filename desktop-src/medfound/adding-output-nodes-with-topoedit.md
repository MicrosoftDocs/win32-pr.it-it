---
description: Aggiunta di nodi di output con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Aggiunta di nodi di output con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306760"
---
# <a name="adding-output-nodes-with-topoedit"></a>Aggiunta di nodi di output con TopoEdit

In una topologia un nodo di output rappresenta un sink multimediale che riceve i dati multimediali da un nodo di trasformazione e li presenta per la riproduzione. Il tipo di nodo di output dipende dal tipo di supporto del nodo di origine.

Nella tabella seguente viene illustrato il comando menu/barra degli strumenti per aggiungere un nodo di output alla topologia.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di supporto di origine</th>
<th>Comando menu/barra degli strumenti</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Flusso audio</td>
<td>Scegliere <strong>Aggiungi SAR</strong>dal menu <strong>topologia</strong> .</td>
<td>Crea un nodo di output per il renderer di streaming audio (SAR) che riproduce un flusso audio tramite un dispositivo audio, ad esempio una scheda audio.</td>
</tr>
<tr class="even">
<td>Flusso video</td>
<td>Nel menu <strong>topologia</strong> fare clic su <strong>Aggiungi EVR</strong>.</td>
<td>Crea un nodo di output per il renderer video avanzato (EVR) che Visualizza i frame per un flusso video.</td>
</tr>
<tr class="odd">
<td>Sink di supporti personalizzati</td>
<td><ol>
<li>Scegliere <strong>Aggiungi sink personalizzato</strong>dal menu <strong>topologia</strong> .<br/> Verrà visualizzata la finestra di dialogo <strong>GUID personalizzato di input</strong> .<br/></li>
<li><p>Nel campo <strong>GUID:</strong> immettere il GUID del sink personalizzato che si desidera aggiungere alla topologia.<br/></p>
<blockquote>
[!Note]<br />
TopoEdit prevede il GUID nel formato &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; . In caso contrario, non sarà possibile aggiungere il nodo e verrà visualizzato un &quot; messaggio di errore GUID non valido &quot; .
</blockquote>
<p><br/></p></li>
<li>Fare clic su <strong>OK</strong>.<br/></li>
</ol></td>
<td>Crea un nodo di output per il sink di flusso per un'origine multimediale personalizzata.<br/> Il sink personalizzato deve supportare <strong>CoCreateInstance</strong> , in modo che il sink possa essere specificato con un CLSID.<br/></td>
</tr>
</tbody>
</table>



 

TopoEdit crea il nodo di output specificato. Il **riquadro topologia** Mostra il nodo output come una casella verde che mostra il nome del sink di flusso.

Per informazioni sull'aggiunta di nodi di output a livello di codice usando le API di Media Foundation, vedere [creazione di nodi di output](creating-output-nodes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Renderer audio di streaming](streaming-audio-renderer.md)
</dt> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




