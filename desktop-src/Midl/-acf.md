---
title: Opzione /acf
description: L'opzione /acf consente all'utente di specificare un nome di file ACF esplicito. L'opzione consente anche l'uso di nomi di interfaccia diversi nei file IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- Opzione /acf MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37248ac346350f618eebc5ca81af144ecee91ce2acf40c39b9e980b574df4764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386128"
---
# <a name="acf-switch"></a>Opzione /acf

**L'opzione /acf** consente all'utente di specificare un nome di file ACF esplicito. L'opzione consente anche l'uso di nomi di interfaccia diversi nei file IDL e ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*acf \_ filename* 
</dt> <dd>

Specifica il nome del file ACF. Gli spazi vuoti possono essere presenti o meno tra **l'opzione /acf** e il nome del file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il compilatore MIDL costruisce il nome del file ACF sostituendo l'estensione di file IDL (in genere con estensione idl) con .acf. Quando è **presente l'opzione /acf,** il file ACF prende il nome dal nome file specificato. **L'opzione /acf** si applica solo al file IDL specificato nella riga di comando del compilatore MIDL. Non si applica ai file importati.

Quando si **usa l'opzione /acf,** il nome dell'interfaccia in ACF non deve corrispondere al nome dell'interfaccia MIDL. Questa funzionalità consente alle interfacce di condividere una specifica ACF.

Quando non viene specificato un percorso assoluto per un file ACF, il compilatore MIDL cerca nella directory corrente, nelle directory fornite dall'opzione [**/I**](-i.md) e nelle directory nel percorso INCLUDE.

Se il file ACF non viene trovato, il compilatore MIDL presuppone che non sia presente alcun ACF per questa interfaccia. Per altre informazioni sulla sequenza di directory, vedere le voci di riferimento per le opzioni [**/I**](-i.md) e [**/no \_ def \_ idir.**](-no-def-idir.md) Per altre informazioni relative a **/acf,** vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

## <a name="examples"></a>Esempio

**midl /acf bar.acf filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/i**](-i.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




