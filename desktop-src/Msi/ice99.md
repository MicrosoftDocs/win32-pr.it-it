---
description: ICE99 verifica che nessun nome di proprietà immesso nella tabella di directory duplica un nome riservato per l'utilizzo pubblico o privato del Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757040"
---
# <a name="ice99"></a>ICE99

ICE99 verifica che nessun nome di proprietà immesso nella tabella di [directory](directory-table.md) duplica un nome riservato per l'utilizzo pubblico o privato del Windows Installer.

## <a name="result"></a>Risultato

ICE99 invia il seguente errore.



| Errore ICE99                                                                                                      | Descrizione                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Il nome della directory: \[ 1 \] corrisponde a una delle proprietà pubbliche MSI e può causare effetti collaterali imprevisti. | Il valore nella colonna directory della tabella [directory](directory-table.md) Duplica il nome di una proprietà riservata dal Windows Installer. |



 

## <a name="example"></a>Esempio

ICE99 segnala l'errore seguente per l'esempio:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Directory](directory-table.md) (parziale)



| Directory        | \_Padre directory | DefaultDir |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

Per correggere il problema, è necessario modificare il nome di CustomActionData.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> <dt>

[Tabella directory](directory-table.md)
</dt> <dt>

[Non supportato in Windows Installer 3,0 e versioni precedenti](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



