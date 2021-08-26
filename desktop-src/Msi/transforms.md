---
description: La proprietà TRANSFORMS è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: TRANSFORMS - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474317"
---
# <a name="transforms-property"></a>TRANSFORMS - proprietà

La **proprietà TRANSFORMS** è un elenco delle trasformazioni applicate dal programma di installazione durante l'installazione del pacchetto. Il programma di installazione applica le trasformazioni nello stesso ordine in cui sono elencate nella proprietà . Le trasformazioni possono essere specificate in base al nome file o al percorso completo. Per specificare più trasformazioni, separare ogni nome file o percorso completo con un punto e virgola (;). Ad esempio, per applicare tre trasformazioni a un pacchetto, impostare **TRANSFORMS** su un elenco di nomi di file o su un elenco di percorsi completi.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

È possibile indicare che un file di trasformazione è incorporato in una risorsa di archiviazione del file .msi, anziché come file autonomo, antefizzando il nome del file con i due punti (:). Ad esempio, l'esempio seguente indica che transform1.mst e transform2.mst sono incorporati nel file .msi e che transform3.mst è un file autonomo.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Il programma di installazione richiede le trasformazioni elencate in **TRANSFORMS** a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto. I [criteri TransformsSecure,](transformssecure-policy.md) la proprietà **TRANSFORMS** e il primo carattere della stringa **TRANSFORMS** informano il programma di installazione come gestire la resilienza di origine dei file di trasformazione autonomi. Windows Il programma di installazione [considera l'impostazione dei criteri TransformsAtSource](transformsatsource-policy.md) [**o TRANSFORMSATSOURCE**](transformsatsource.md) come transformsSecure policy e [**TRANSFORMSSECURE**](transformssecure.md). Si noti che le trasformazioni incorporate nel file .msi non vengono memorizzate nella cache e vengono sempre ottenute dal pacchetto.




| Proprietà TRANSFORMS | Trasformazioni protette | Caching e resilienza | 
|---------------------|-------------------|------------------------|
| @[<em>elenco di nomi di file</em>] Esempio:<br /> @transform1.mst;transform2.mst; transform3.mst<br /> | Nessun effetto. | <a href="secure-at-source-transforms.md">Trasformazioni secure-at-source</a>. L'origine delle trasformazioni deve essere nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico alla ricerca di un file .msi di origine. Vedere <a href="source-resiliency.md">Resilienza dell'origine.</a> | 
| |[<em>elenco di percorsi</em>] Esempio:<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst; \\ server2\share2\path2\transform2.mst</code></pre> | Nessun effetto. | <a href="secure-full-path-transforms.md">Trasformazioni secure-full-path</a>. L'origine di ogni trasformazione deve essere nel percorso completo passato a <strong>TRANSFORMS.</strong> Non è necessario che l'origine della trasformazione si trovi nell'origine del pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni nel computer dell'utente in una cache in cui l'utente non ha accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, il programma di installazione può ripristinare la cache solo dall'origine nel percorso specificato. | 
| [<em>elenco di nomi di file</em>] Il primo carattere non è @ o |.<br /> Esempio:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformsSecure policy</a> or <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> impostato su 1 OR<br /><a href="transformsatsource-policy.md">Criteri TransformsAtSource</a> o <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> impostati su 1.<br /> | Se <strong>TRANSFORMS è</strong> un elenco di nomi di file, il programma di installazione li considera come trasformazioni <a href="secure-at-source-transforms.md">Secure-At-Source</a>. Se <strong>TRANSFORMS è</strong> un elenco di percorsi completi, il programma di installazione li considera come trasformazioni <a href="secure-full-path-transforms.md">secure-full-path</a>.<br /> | 
| [<em>elenco di nomi di file</em>] Il primo carattere non è @ o |.<br /> Esempio:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformsSecure policy</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati su AND<br /><a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> e <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> non sono impostati.<br /> | <a href="unsecured-transforms.md">Trasformazioni non protette</a>. L'origine delle trasformazioni deve essere nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di eseguire il roaming tra computer mantenendo le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella %windir%\Installer. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico alla ricerca di un file .msi di origine. Vedere <a href="source-resiliency.md">Resilienza dell'origine.</a> | 
| [<em>elenco di percorsi</em>] Il primo carattere non è @ o |.<br /> Esempio:<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | <a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati su AND<br /><a href="transformsatsource-policy.md">I criteri TransformsAtSource</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> non sono impostati.<br /> | <a href="unsecured-transforms.md">Trasformazioni non protette</a>. Quando il pacchetto viene installato o annunciato per utente, il programma di installazione salva le trasformazioni nel profilo dell'utente. Ciò consente a un utente di eseguire il roaming tra computer mantenendo le personalizzazioni. Per un'installazione per computer, la trasformazione viene salvata nella cartella %windir%\Installer. Se la copia locale della trasformazione non è più disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico alla ricerca di un file .msi di origine. Vedere <a href="source-resiliency.md">Resilienza dell'origine.</a> | 




 

Non è possibile usare nomi file e percorsi nello stesso **elenco TRANSFORMS.** Non è possibile specificare trasformazioni protette e profilate nello stesso elenco. È possibile includere le trasformazioni incorporate nel pacchetto in un elenco con altre trasformazioni.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Si noti che poiché il delimitatore di elenco per le trasformazioni è il carattere punto e virgola, i punti e virgola non devono essere usati in un percorso o in un nome file di trasformazione.

## <a name="remarks"></a>Commenti

Nei casi in cui il criterio [TransformsSecure](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) è stata impostata con Windows Installer, non è necessario passare il simbolo @ o quando si imposta TRANSFORMS tramite la riga di \| comando.  Il programma di installazione presuppone Secure-At-Source o Secure-Full-Path se l'elenco è costituito interamente da nomi di file che si trovano nell'origine o è costituito interamente da percorsi completi. Non è comunque possibile combinare i due tipi di origini di trasformazione.

Si noti che il programma di installazione usa un ordine di ricerca diverso per le trasformazioni non protette applicate durante le prime installazioni di manutenzione. Per altre informazioni, vedere [Trasformazioni non protette.](unsecured-transforms.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Trasformazioni del database](database-transforms.md)
</dt> <dt>

[Unioni e trasformazioni](merges-and-transforms.md)
</dt> <dt>

[Resilienza dell'origine](source-resiliency.md)
</dt> </dl>

 

 




