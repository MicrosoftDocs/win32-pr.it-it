---
title: /n (opzione)
description: L'opzione/n specifica la profondità della composizione per la composizione dei file di metadati.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331934"
---
# <a name="n-switch"></a>/n (opzione)

L'opzione **/n** specifica la profondità della composizione per la composizione dei file di metadati.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*profondità dello spazio dei nomi \_* 
</dt> <dd>

Specifica la profondità dello spazio dei nomi da comporre in un unico file di metadati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Di seguito sono riportati i possibili formati di valore che è possibile specificare con l'opzione **/n** .



| Formato del valore                   | Descrizione                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Comporre tutti i tipi in corrispondenza della profondità dello spazio dei nomi specificata nell'opzione.               |
| -1                             | Comporre tutti i tipi in un file IDL per ogni spazio dei nomi.                              |
| <namespace>: Int32 > 0 | Comporre tutti i tipi con lo spazio dei nomi corrispondente alla profondità specificata nell'opzione. |
| <namespace>:-1           | Comporre tutti i tipi con lo spazio dei nomi corrispondente in un unico file per spazio dei nomi.          |



 

Nella tabella seguente vengono illustrati i risultati di diverse combinazioni dell'opzione **/n** che opera su questi spazi dei nomi.

-   Windows. Foundation. Collections. all'IIterable
-   Windows. UI. DirectUI. Controls. Button
-   Windows. UI. DirectUI. Controls. ListView
-   Windows. UI. immersive. Application. PlayToSpazio. target
-   Windows. Web. Syndication. RSS



| Commutatori                         | Risultato                                                                                                                                                                                                                                                       | Spiegazione                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | L'ultima opzione/n esegue l'override di tutte le opzioni-n precedenti.                                                                                                                                                                                                                                                                           |
| **/n:-1/n: Windows. UI: 2**         | <dl> Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. winmd</dt> <dt>Windows. Web. Syndication. winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** è sempre composto in – n:2.</dt> <dt>I tipi **Windows. UI** sono raggruppati.</dt> <dt>**Windows. Web. Syndication** è costituito in n:-1.</dt> </dl>       |
| **/n: 1/n: Windows. UI. DirectUI: 3** | <dl> Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. directui. winmd</dt> <dt>Windows. winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** è sempre composto in – n:2.</dt> <dt>**Windows. UI. directui** è composto al livello 3.</dt> <dt>Tutti gli altri tipi sono composti al livello 1.</dt> </dl> |



 

Di seguito sono riportate le regole per la gestione di più istanze dell'opzione **/n** .

-   L'istanza più specifica prevale. Se ad esempio si specifica **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE risolve a. b. c. D al livello 4, perché a. b. c è più specifico di A.B. A. B. E. F viene risolto alla profondità 5, perché corrisponde A un. B ma non a A.B.C.
-   L'ultima istanza prevale. Se ad esempio si specifica **– n:5 – n:2**, i tipi sono composti al livello 2.
-   Entrambe le regole si applicano. Se si specifica – n:A.B.C: 4 – n:A.B.C: 1, lo spazio dei nomi A. B. C viene composto al livello 1.

## <a name="examples"></a>Esempio

**mdmerge.exe-Metadata \_ dir $ ( \_ percorso metadati SDK \_ )-i $ ( \_ percorso metadati interno SDK \_ \_ )-o $ ( \_ percorso obj) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation: 2**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





