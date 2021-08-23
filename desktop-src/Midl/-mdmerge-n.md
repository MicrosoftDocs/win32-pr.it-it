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
ms.openlocfilehash: d3e9575995d80a4c61b5e91be7c5cfc1c802abed892af8cfa653f62c66e602b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430971"
---
# <a name="n-switch"></a>Opzione /n

**L'opzione /n** specifica la profondità di composizione per la composizione dei file di metadati.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*profondità dello spazio \_ dei nomi* 
</dt> <dd>

Specifica la profondità dello spazio dei nomi da comporre in un singolo file di metadati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ecco i possibili formati di valore che è possibile specificare con **l'opzione /n.**



| Formato del valore                   | Descrizione                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Comporre tutti i tipi alla profondità dello spazio dei nomi specificata nell'opzione .               |
| -1                             | Comporre tutti i tipi in un unico file IDL per ogni spazio dei nomi.                              |
| <namespace>:Int32 > 0 | Comporre tutti i tipi con lo spazio dei nomi corrispondente alla profondità specificata nell'opzione . |
| <namespace>:-1           | Comporre tutti i tipi con spazio dei nomi corrispondente in un unico file per ogni spazio dei nomi.          |



 

Nella tabella seguente vengono illustrati i risultati di diverse combinazioni **dell'opzione /n** che opera su questi spazi dei nomi.

-   Windows. Foundation.Collections.IIterable
-   Windows. Ui. DirectUI.Controls.Button
-   Windows. Ui. DirectUI.Controls.ListView
-   Windows. Ui. Immersive.Application.PlayTo.Target
-   Windows. Web.Syndication.RSS



| Commutatori                         | Risultato                                                                                                                                                                                                                                                       | Spiegazione                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | L'ultima opzione /n esegue l'override di tutte le opzioni -n precedenti.                                                                                                                                                                                                                                                                           |
| **/n:-1/n:Windows. Interfaccia utente:2**         | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. Ui.winmd</dt> <dt>Windows. Web.Syndication.winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** è sempre composto da –n:2.</dt> <dt>**Windows. I tipi** di interfaccia utente sono raggruppati.</dt> <dt>**Windows. Web.Syndication** è composto in n:-1.</dt> </dl>       |
| **/n:1/n:Windows. Ui. DirectUI:3** | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. Ui. DirectUI.winmd</dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** è sempre composto da –n:2.</dt> <dt>**Windows. Ui. DirectUI** è composto al livello 3.</dt> <dt>Tutti gli altri tipi sono composti al livello 1.</dt> </dl> |



 

Ecco le regole per la gestione di più istanze **dell'opzione /n.**

-   Istanza più specifica. Ad esempio, se si specifica **–n:A.B.C:4-n:A.B:5,** MDMERGE risolve A.B.C.D al livello 4, perché A.B.C è più specifico di A.B. A.B.E.F si risolve alla profondità 5, perché corrisponde ad A.B ma non ad A.B.C.
-   L'ultima istanza è di tipo . Ad esempio, se si specifica **–n:5-n:2**, i tipi sono composti al livello 2.
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

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





