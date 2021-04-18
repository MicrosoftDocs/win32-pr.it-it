---
description: La proprietà Transforms è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Proprietà Transforms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abbb45db507f7ab813b96e9023634cbe217b554
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330915"
---
# <a name="transforms-property"></a>Proprietà Transforms

La proprietà **TRANSforms** è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto. Il programma di installazione applica le trasformazioni nello stesso ordine in cui sono elencate nella proprietà. Le trasformazioni possono essere specificate in base al nome file o al percorso completo. Per specificare più trasformazioni, separare il nome file o il percorso completo con un punto e virgola (;). Ad esempio, per applicare tre trasformazioni a un pacchetto, impostare le **TRASformazioni** in un elenco di nomi di file o in un elenco di percorsi completi.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

È possibile indicare che un file di trasformazione è incorporato in un'archiviazione del file con estensione msi, anziché come file autonomo, anteponendo il nome del file con i due punti (:). Ad esempio, l'esempio seguente indica che transform1. MST e transform2. MST sono incorporati nel file con estensione msi e che transform3. MST è un file autonomo.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Il programma di installazione richiede che le trasformazioni siano elencate in **TRASformazioni** a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto. Il criterio del [criterio TRANSFORMSSECURE](transformssecure-policy.md) , la proprietà **transforms** e il primo carattere della stringa **Transformations** informa il programma di installazione come gestire la resilienza di origine dei file di trasformazione autonomi. Windows Installer considera l'impostazione dei [criteri TransformsAtSource](transformsatsource-policy.md) o [**TransformsAtSource**](transformsatsource.md) uguale a TRANSFORMSSECURE Policy e [**TRANSFORMSSECURE**](transformssecure.md). Si noti che le trasformazioni incorporate nel file con estensione msi non vengono memorizzate nella cache e vengono sempre ottenute dal pacchetto.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà Transforms</th>
<th>Trasformazioni sicure</th>
<th>Memorizzazione nella cache e resilienza</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@ [<em>elenco di nomi file</em>] esempio:<br/> @transform1.mst; transform2. MST; transform3. MST<br/></td>
<td>Nessun effetto.</td>
<td><a href="secure-at-source-transforms.md">Trasformazioni protette a livello di origine</a>. L'origine delle trasformazioni deve trovarsi nella radice dell'origine del pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non dispone dell'accesso in scrittura. Se la copia locale della trasformazione diventa non disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico a quello di ricerca nell'elenco di origine di un file con estensione msi. Vedere <a href="source-resiliency.md">resilienza del codice sorgente</a>.</td>
</tr>
<tr class="even">
<td>| [<em>elenco di percorsi</em>] Esempio<br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td>Nessun effetto.</td>
<td><a href="secure-full-path-transforms.md">Trasformazioni protette con percorso completo</a>. L'origine di ogni trasformazione deve trovarsi nel percorso completo passato alle <strong>TRASformazioni</strong>. Non è necessario che l'origine della trasformazione si trovi nell'origine del pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non dispone dell'accesso in scrittura. Se la copia locale della trasformazione diventa non disponibile, il programma di installazione può ripristinare solo la cache dall'origine nel percorso specificato.</td>
</tr>
<tr class="odd">
<td>[<em>elenco di nomi file</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td>Il <a href="transformssecure-policy.md">criterio TRANSFORMSSECURE</a> o <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> è impostato su 1 o<br/> Il <a href="transformsatsource-policy.md">criterio TransformsAtSource</a> o <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> è impostato su 1.<br/></td>
<td>Se <strong>TRASformazioni</strong> è un elenco di nomi di file, il programma di installazione li considera come <a href="secure-at-source-transforms.md">trasformazioni sicure all'origine</a>. Se <strong>TRASformazioni</strong> è un elenco di percorsi completi, il programma di installazione li considera come <a href="secure-full-path-transforms.md">trasformazioni con percorso completo protetto</a>.<br/></td>
</tr>
<tr class="even">
<td>[<em>elenco di nomi file</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td>I <a href="transformssecure-policy.md">criteri di TRANSFORMSSECURE</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati e<br/> I <a href="transformsatsource-policy.md">criteri TransformsAtSource</a> e <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> non sono impostati.<br/></td>
<td><a href="unsecured-transforms.md">Trasformazioni non protette</a>. L'origine delle trasformazioni deve trovarsi nella radice dell'origine del pacchetto. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di spostarsi tra i computer, mantenendo al tempo stesso le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella%windir%\Installer. Se la copia locale della trasformazione diventa non disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico a quello di ricerca nell'elenco di origine di un file con estensione msi. Vedere <a href="source-resiliency.md">resilienza del codice sorgente</a>.</td>
</tr>
<tr class="odd">
<td>[<em>elenco di percorsi</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td>I <a href="transformsatsource-policy.md">criteri di TransformsAtSource</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati e<br/> I <a href="transformsatsource-policy.md">criteri TransformsAtSource</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati.<br/></td>
<td><a href="unsecured-transforms.md">Trasformazioni non protette</a>. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di spostarsi tra i computer, mantenendo al tempo stesso le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella%windir%\Installer. Se la copia locale della trasformazione diventa non disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico a quello di ricerca nell'elenco di origine di un file con estensione msi. Vedere <a href="source-resiliency.md">resilienza del codice sorgente</a>.</td>
</tr>
</tbody>
</table>



 

Non è possibile utilizzare i nomi file e i percorsi insieme nello stesso elenco di **TRASformazioni** . Non è possibile specificare le trasformazioni sicure e del profilo insieme nello stesso elenco. È possibile includere trasformazioni incorporate nel pacchetto in un elenco con altre trasformazioni.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Si noti che poiché il delimitatore di elenco per le trasformazioni è il carattere punto e virgola, i punti e virgola non devono essere utilizzati in un percorso o un nome file di trasformazione.

## <a name="remarks"></a>Commenti

Nei casi in cui il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) è stata impostata con Windows Installer, non è necessario passare il simbolo @ o quando si impostano le \| **trasformazioni** tramite la riga di comando. Se l'elenco è costituito interamente da nomi di file che si trovano nell'origine o è costituito interamente da percorsi completi, il programma di installazione presuppone che il percorso sia sicuro a livello di origine o protetto. Non è ancora possibile combinare i due tipi di origini di trasformazione.

Si noti che il programma di installazione usa un ordine di ricerca diverso per le trasformazioni non protette applicate durante la prima installazione e la manutenzione. Per altre informazioni, vedere [trasformazioni non protette](unsecured-transforms.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> <dt>

[Unioni e trasformazioni](merges-and-transforms.md)
</dt> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




