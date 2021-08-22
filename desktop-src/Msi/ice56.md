---
description: ICE56 verifica che la struttura di directory del file .msi abbia una singola directory radice, che la radice sia la proprietà TARGETDIR e che il valore della proprietà SourceDir si trova nella colonna DefaultDir della tabella Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c1feb3e3dbab84a58809496b28a60d3a2436c3041d3a2d58f0ac8f2b5e47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528221"
---
# <a name="ice56"></a>ICE56

ICE56 verifica che la struttura di directory del file .msi abbia una singola directory radice, che la radice sia la proprietà [**TARGETDIR**](targetdir.md) e che il valore della proprietà [**SourceDir**](sourcedir.md) si trova nella colonna DefaultDir della [tabella Directory](directory-table.md).

Se un .msi file ha più radici o specifica una radice [](administrative-installation.md) diversa da [**TARGETDIR,**](targetdir.md)un'installazione amministrativa non crea un'immagine amministrativa corretta.

Si noti che le directory vuote non vengono controllate da ICE56. La struttura di directory supera la convalida con più directory radice se le directory aggiuntive sono vuote.

## <a name="result"></a>Risultato

ICE56 invia un errore se il .msi non ha una singola radice, [**TARGETDIR**](targetdir.md)o se [**SourceDir**](sourcedir.md) non è specificato nella colonna DefaultDir della [tabella Directory](directory-table.md).

## <a name="example"></a>Esempio

ICE56 segnala gli errori seguenti per l'esempio illustrato.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Tabella directory](directory-table.md)



| Directory | Padre \_ della directory | DefaultDir |
|-----------|-------------------|------------|
| Targetdir |                   | Temp       |
| Radice2     | Radice2             | SourceDir  |



 

Per correggere il primo errore, la radice [**TARGETDIR**](targetdir.md) deve avere un valore DefaultDir di [**SourceDir**](sourcedir.md). Viene accettato anche SOURCEDIR. Potrebbe essere possibile impostare **TARGETDIR** come padre della seconda radice e usare il valore '.' nella colonna DefaultDir. Per altre [informazioni, vedere](directory-table.md) la tabella Directory.

Per correggere il secondo errore, la struttura directory deve avere una sola radice denominata [**TARGETDIR**](targetdir.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



