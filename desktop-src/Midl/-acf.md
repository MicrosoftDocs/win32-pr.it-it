---
title: opzione/ACF
description: L'opzione/ACF consente all'utente di specificare un nome di file ACF esplicito. L'opzione consente inoltre l'utilizzo di nomi di interfaccia diversi nei file IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF switch MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955995"
---
# <a name="acf-switch"></a>opzione/ACF

L'opzione **/ACF** consente all'utente di specificare un nome di file ACF esplicito. L'opzione consente inoltre l'utilizzo di nomi di interfaccia diversi nei file IDL e ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*\_nome file ACF* 
</dt> <dd>

Specifica il nome dell'oggetto ACF. Gli spazi vuoti possono essere presenti tra l'opzione **/ACF** e il nome file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il compilatore MIDL costruisce il nome dell'ACF sostituendo l'estensione del nome file IDL (in genere IDL) con. ACF. Quando l'opzione **/ACF** è presente, l'ACF prende il nome dal nome file specificato. L'opzione **/ACF** si applica solo al file idl specificato nella riga di comando del compilatore MIDL. Non si applica ai file importati.

Quando si usa l'opzione **/ACF** , il nome dell'interfaccia in ACF non deve corrispondere al nome dell'interfaccia MIDL. Questa funzionalità consente alle interfacce di condividere una specifica ACF.

Quando non viene specificato un percorso assoluto di un ACF, il compilatore MIDL Cerca nella directory corrente le directory fornite dall'opzione [**/i**](-i.md) e le directory nel percorso di inclusione.

Se l'ACF non viene trovato, il compilatore MIDL presuppone che non esista alcun ACF per questa interfaccia. Per ulteriori informazioni sulla sequenza di directory, vedere le voci di riferimento per le opzioni [**/i**](-i.md) e [**/No \_ def \_ Idir**](-no-def-idir.md) . Per ulteriori informazioni relative a **/ACF**, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Esempio

**MIDL/ACF bar. ACF nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/No \_ def \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 




