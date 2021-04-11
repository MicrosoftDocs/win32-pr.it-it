---
title: opzione/LCID
description: L'opzione del compilatore MIDL/LCID consente di usare i caratteri internazionali nei file di input, nei nomi file e nei percorsi di directory.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID switch MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334559"
---
# <a name="lcid-switch"></a>opzione/LCID

L'opzione del compilatore MIDL **/LCID** consente di usare i caratteri internazionali nei file di input, nei nomi file e nei percorsi di directory.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*localeID* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali a 32 bit utilizzato nel supporto della lingua nazionale di Windows. L'identificatore delle impostazioni locali deve essere specificato in decimale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nei file di input è possibile utilizzare commenti, stringhe, HelpStrings e identificatori localizzati. In particolare, l'opzione **/LCID** fornisce un supporto DBCS completo, per rappresentare lingue asiatiche quali giapponese, cinese e coreano.

> [!Note]  
> L'opzione **/LCID** è disponibile con MIDL versione 3.01.75 e versioni successive.

 

## <a name="examples"></a>Esempio

**MIDL/LCID 1041 iface. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> </dl>

 

 




