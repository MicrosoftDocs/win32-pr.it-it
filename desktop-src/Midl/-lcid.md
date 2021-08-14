---
title: Opzione /lcid
description: L'opzione del compilatore MIDL /lcid consente di usare caratteri internazionali nei file di input, nei nomi di file e nei percorsi di directory.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- Opzione /lcid MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385514"
---
# <a name="lcid-switch"></a>Opzione /lcid

L'opzione del compilatore MIDL **/lcid** consente di usare caratteri internazionali nei file di input, nei nomi di file e nei percorsi di directory.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Localeid* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali a 32 bit usato in Windows national language support. L'identificatore delle impostazioni locali deve essere specificato in formato decimale.

</dd> </dl>

## <a name="remarks"></a>Commenti

All'interno dei file di input è possibile usare commenti, stringhe, helpstring e identificatori localizzati. In particolare, **l'opzione /lcid** fornisce il supporto DBCS completo per rappresentare le lingue dell'Asia, ad esempio giapponese, cinese e coreano.

> [!Note]  
> **L'opzione /lcid** è disponibile con MIDL versione 3.01.75 e successive.

 

## <a name="examples"></a>Esempio

**midl /lcid 1041 iface.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> </dl>

 

 




