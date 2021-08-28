---
title: Opzione /n
description: L'opzione /n specifica la profondità di composizione per la composizione dei file di metadati.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- Opzione /n MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b54473b282976d2ab871db0f1699c1154070a3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886032"
---
# <a name="n-switch"></a>Opzione /n

**L'opzione /n** specifica la profondità di composizione per la composizione dei file di metadati.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*profondità dello \_ spazio dei nomi* 
</dt> <dd>

Specifica la profondità dello spazio dei nomi da comporre in un singolo file di metadati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ecco i possibili formati di valore che è possibile specificare con **l'opzione /n.**



| Formato del valore                   | Descrizione                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Comporre tutti i tipi alla profondità dello spazio dei nomi specificata nell'opzione .               |
| -1                             | Comporre tutti i tipi in un unico file IDL per ogni spazio dei nomi.                              |
| &lt;namespace &gt; :Int32 > 0 | Comporre tutti i tipi con lo spazio dei nomi corrispondente alla profondità specificata nell'opzione . |
| &lt;spazio &gt; dei nomi :-1           | Comporre tutti i tipi con spazio dei nomi corrispondente in un unico file per ogni spazio dei nomi.          |



 

La tabella seguente mostra i risultati di diverse combinazioni **dell'opzione /n** che lavora su questi spazi dei nomi.

-   Windows. Foundation.Collections.IIterable
-   Windows. UI. DirectUI.Controls.Button
-   Windows. UI. DirectUI.Controls.ListView
-   Windows. UI. Immersive.Application.PlayTo.Target
-   Windows. Web.Syndication.RSS



| Commutatori                         | Risultato                                                                                                                                                                                                                                                       | Spiegazione                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | L'ultima opzione /n esegue l'override di tutte le opzioni –n precedenti.                                                                                                                                                                                                                                                                           |
| **/n:-1/n:Windows. Interfaccia utente:2**         | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. Ui.winmd Windows.</dt> <dt> Web.Syndication.winmd</dt> </dl> | <dl> <dt>**Windows. La** base è sempre composta da –n:2.</dt> <dt>**Windows. I tipi** di interfaccia utente sono raggruppati.</dt> <dt>**Windows. Web.Syndication** è costituito da n:-1.</dt> </dl>       |
| **/n:1/n:Windows. UI. DirectUI:3** | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. UI. DirectUI.winmd</dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows. La** base è sempre composta da –n:2.</dt> <dt>**Windows. UI. DirectUI** è composto al livello 3.</dt> <dt>Tutti gli altri tipi sono composti al livello 1.</dt> </dl> |



 

Ecco le regole per la gestione di più istanze **dell'opzione /n.**

-   Prevale l'istanza più specifica. Ad esempio, se si specifica **–n:A.B.C:4-n:A.B:5,** MDMERGE risolve A.B.C.D al livello 4, perché A.B.C è più specifico di A.B. A.B.E.F viene risolto alla profondità 5, perché corrisponde a A.B ma non a A.B.C.
-   Prevale l'ultima istanza. Ad esempio, se si specifica **–n:5-n:2,** i tipi sono composti al livello 2.
-   Entrambe queste regole si applicano. Se si specifica –n:A.B.C:4 –n:A.B.C:1, lo spazio dei nomi A.B.C è composto al livello 1.

## <a name="examples"></a>Esempio

**mdmerge.exe -metadata \_ dir $(SDK \_ METADATA \_ PATH) -i $(INTERNAL \_ SDK METADATA \_ \_ PATH) -o $(OBJ \_ PATH) $O \\ \\ SystemMetadata -v -n:-1 -n:Windows. Base:2**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





