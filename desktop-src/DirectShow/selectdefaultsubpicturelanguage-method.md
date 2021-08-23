---
description: Il metodo SelectDefaultSubpictureLanguage imposta la lingua dell'immagine secondaria predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Metodo SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aaa6b927d33626299258ac54136e1a67b0dedb40427a35d9c79465be3e9a15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072585"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Metodo SelectDefaultSubpictureLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectDefaultSubpictureLanguage` metodo imposta la lingua dell'immagine secondaria predefinita corrente nell'oggetto **MSWebDVD.**

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*Ilang*
</dt> <dd>

Specifica la lingua come integer.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Specifica l'estensione del linguaggio dell'immagine secondaria come integer.



| Valore | Descrizione                    |
|-------|--------------------------------|
| 0     | Estensione non specificata        |
| 1     | Didascalie normali                |
| 2     | Big Caption                   |
| 3     | Didascalie per bambini            |
| 5     | Sottotitoli codificati normali         |
| 6     | Sottotitoli codificati grandi            |
| 7     | Sottotitoli codificati per bambini     |
| 9     | Forced                         |
| 13    | Commenti del direttore normale     |
| 14    | Commenti di Big Director        |
| 15    | Commenti del direttore dei bambini |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'estensione del linguaggio delle immagini secondarie fornisce altre informazioni sull'immagine secondaria.

 

 



