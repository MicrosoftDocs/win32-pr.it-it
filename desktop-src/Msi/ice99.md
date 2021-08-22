---
description: ICE99 verifica che nessun nome di proprietà immesso nella tabella Directory duplici un nome riservato per l'uso pubblico o privato del Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315271"
---
# <a name="ice99"></a>ICE99

ICE99 verifica che nessun nome di proprietà immesso nella tabella [Directory](directory-table.md) duplici un nome riservato per l'uso pubblico o privato del Windows Installer.

## <a name="result"></a>Risultato

ICE99 invia l'errore seguente.



| Errore ICE99                                                                                                      | Descrizione                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Il nome della directory: 1 corrisponde a una delle proprietà pubbliche dell'msi e può causare effetti \[ \] collaterali imprevisti. | Il valore nella colonna Directory della tabella [Directory](directory-table.md) duplica un nome di proprietà riservato dal Windows Installer. |



 

## <a name="example"></a>Esempio

ICE99 segnala l'errore seguente per l'esempio:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Directory](directory-table.md) (parziale)



| Directory        | Padre \_ della directory | DefaultDir |
|------------------|-------------------|------------|
| Customactiondata |                   |            |



 

Per correggere questo avviso, è necessario modificare il nome di CustomActionData.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> <dt>

[Tabella directory](directory-table.md)
</dt> <dt>

[Non supportato in Windows Installer 3.0 e versioni precedenti](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



