---
description: ICE56 verifica che la struttura di directory del file con estensione msi disponga di una singola directory radice, che la radice sia la proprietà TARGETDIR e che il valore della proprietà SourceDir sia presente nella colonna DefaultDir della tabella di directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315904"
---
# <a name="ice56"></a>ICE56

ICE56 verifica che la struttura di directory del file con estensione msi disponga di una singola directory radice, che la radice sia la proprietà [**targetdir**](targetdir.md) e che il valore della proprietà [**SourceDir**](sourcedir.md) sia presente nella colonna DefaultDir della [tabella di directory](directory-table.md).

Se un file con estensione MSI ha più radici o specifica una radice diversa da [**targetdir**](targetdir.md), un' [installazione amministrativa](administrative-installation.md) non crea un'immagine amministrativa corretta.

Si noti che le directory vuote non vengono controllate da ICE56. La struttura di directory passa la convalida a più directory radice se le directory aggiuntive sono vuote.

## <a name="result"></a>Risultato

ICE56 Invia un errore se il file con estensione msi non dispone di una sola radice, [**targetdir**](targetdir.md)o se [**SourceDir**](sourcedir.md) non è specificato nella colonna DefaultDir della [tabella di directory](directory-table.md).

## <a name="example"></a>Esempio

ICE56 segnala gli errori seguenti per l'esempio illustrato.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Tabella directory](directory-table.md)



| Directory | \_Padre directory | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| ROOT2     | ROOT2             | SourceDir  |



 

Per correggere il primo errore, la radice [**targetdir**](targetdir.md) deve avere il valore DefaultDir [**SourceDir**](sourcedir.md). Viene inoltre accettata SOURCEDIR. Potrebbe essere possibile rendere **targetdir** il padre della seconda radice e usare il valore ' .' nella colonna DefaultDir. Per ulteriori informazioni, vedere la [tabella directory](directory-table.md) .

Per correggere il secondo errore, la struttura di directory deve avere solo una radice denominata [**targetdir**](targetdir.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



