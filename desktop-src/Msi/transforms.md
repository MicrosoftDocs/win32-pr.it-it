---
description: La proprietà TRANSFORMS è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: TRANSFORMS - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0482e660de981e5071526df9b508d948e74ae910c29df7916ac6e497344447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039421"
---
# <a name="transforms-property"></a>TRANSFORMS - proprietà

La **proprietà TRANSFORMS** è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto. Il programma di installazione applica le trasformazioni nello stesso ordine in cui sono elencate nella proprietà . Le trasformazioni possono essere specificate in base al nome file o al percorso completo. Per specificare più trasformazioni, separare ogni nome file o percorso completo con un punto e virgola (;). Ad esempio, per applicare tre trasformazioni a un pacchetto, impostare **TRANSFORMS** su un elenco di nomi di file o su un elenco di percorsi completi.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

È possibile indicare che un file di trasformazione è incorporato in una risorsa di archiviazione del file .msi, anziché come file autonomo, antendo al nome file i due punti (:). Ad esempio, l'esempio seguente indica che transform1.mst e transform2.mst sono incorporati nel file .msi e che transform3.mst è un file autonomo.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Il programma di installazione richiede le trasformazioni elencate in **TRANSFORMS** a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto. I [criteri TransformsSecure,](transformssecure-policy.md) la proprietà **TRANSFORMS** e il primo carattere della stringa **TRANSFORMS** informano il programma di installazione come gestire la resilienza di origine dei file di trasformazione autonomi. Windows Il programma di installazione [considera l'impostazione dei criteri TransformsAtSource](transformsatsource-policy.md) [**o TRANSFORMSATSOURCE**](transformsatsource.md) come transformsSecure policy [**e TRANSFORMSSECURE.**](transformssecure.md) Si noti che le trasformazioni incorporate nel file .msi non vengono memorizzate nella cache e vengono sempre ottenute dal pacchetto.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà TRANSFORMS</th>
<th>Transforms Secure</th>
<th>Caching e resilienza</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@[<em>elenco di nomi file</em>] Esempio:<br/> @transform1.mst;transform2.mst; transform3.mst<br/></td>
<td>Nessun effetto.</td>
<td><a href="secure-at-source-transforms.md">Trasformazioni secure-at-source</a>. L'origine delle trasformazioni deve essere nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è uguale alla ricerca di un file .msi origine. Vedere <a href="source-resiliency.md">Resilienza di origine.</a></td>
</tr>
<tr class="even">
<td>| [<em>elenco di percorsi</em>] Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td>Nessun effetto.</td>
<td><a href="secure-full-path-transforms.md">Trasformazioni Secure-Full-Path</a>. L'origine di ogni trasformazione deve essere nel percorso completo passato a <strong>TRANSFORMS.</strong> Non è necessario che l'origine della trasformazione si trovi nell'origine del pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, il programma di installazione può ripristinare la cache solo dall'origine nel percorso specificato.</td>
</tr>
<tr class="odd">
<td>[<em>list of filenames</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/> transform1.mst;transform2.mst; transform3.mst<br/></td>
<td><a href="transformssecure-policy.md">TransformsReticurezza dei</a> <a href="transformssecure.md"><strong>criteri o TRANSFORMSSECURE</strong></a> impostata su 1 OR<br/> <a href="transformsatsource-policy.md">TransformsAtSource o</a> <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> impostato su 1.<br/></td>
<td>Se <strong>TRANSFORMS è</strong> un elenco di nomi file, il programma di installazione li considera <a href="secure-at-source-transforms.md">come trasformazioni Secure-At-Source</a>. Se <strong>TRANSFORMS è</strong> un elenco di percorsi completi, il programma di installazione li considera come <a href="secure-full-path-transforms.md">trasformazioni Secure-Full-Path</a>.<br/></td>
</tr>
<tr class="even">
<td>[<em>list of filenames</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/> transform1.mst;transform2.mst; transform3.mst<br/></td>
<td><a href="transformssecure-policy.md">TransformsSecure policy</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati su AND<br/> <a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> <a href="transformsatsource.md"><strong>e TRANSFORMSATSOURCE</strong></a> non sono impostati.<br/></td>
<td><a href="unsecured-transforms.md">Trasformazioni non protette</a>. L'origine delle trasformazioni deve essere nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di eseguire il roaming tra computer mantenendo le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella %windir%\Installer. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è uguale alla ricerca di un file .msi origine. Vedere <a href="source-resiliency.md">Resilienza di origine.</a></td>
</tr>
<tr class="odd">
<td>[<em>elenco di percorsi</em>] Il primo carattere non è @ o |.<br/> Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td><a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> <a href="transformssecure.md"><strong>e TRANSFORMSSECURE</strong></a> non sono impostati su AND<br/> <a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> <a href="transformssecure.md"><strong>e TRANSFORMSSECURE</strong></a> non sono impostati.<br/></td>
<td><a href="unsecured-transforms.md">Trasformazioni non protette</a>. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di eseguire il roaming tra computer mantenendo le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella %windir%\Installer. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è uguale alla ricerca di un file .msi origine. Vedere <a href="source-resiliency.md">Resilienza di origine.</a></td>
</tr>
</tbody>
</table>



 

Non è possibile usare nomi file e percorsi insieme nello stesso **elenco TRANSFORMS.** Non è possibile specificare trasformazioni sicure e di profilo nello stesso elenco. È possibile includere trasformazioni incorporate nel pacchetto in un elenco con altre trasformazioni.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Si noti che poiché il delimitatore di elenco per le trasformazioni è il carattere punto e virgola, il punto e virgola non deve essere usato in un percorso o in un nome file di trasformazione.

## <a name="remarks"></a>Commenti

Nei casi in cui il criterio [TransformsSecure](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) è stata impostata con il programma di installazione di Windows, non è necessario passare il simbolo @ o quando si imposta TRANSFORMS tramite la riga di \| comando.  Il programma di installazione presuppone secure-at-source o secure-full-path se l'elenco è costituito interamente da nomi di file che si trovano nell'origine o è costituito interamente da percorsi completi. Non è comunque possibile combinare i due tipi di origini di trasformazione.

Si noti che il programma di installazione usa un ordine di ricerca diverso per le trasformazioni non protette applicate durante la prima installazione e manutenzione. Per altre informazioni, vedere [Trasformazioni non protette.](unsecured-transforms.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



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

 

 




