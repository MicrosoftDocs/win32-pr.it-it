---
description: Il metodo SelectDefaultSubpictureLanguage imposta la lingua dell'immagine predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Metodo SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746247"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Metodo SelectDefaultSubpictureLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectDefaultSubpictureLanguage` metodo imposta la lingua di immagine predefinita corrente nell'oggetto **mswebdvd** .

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Specifica il linguaggio come intero.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Specifica l'estensione del linguaggio di sottoimmagine come intero.



| Valore | Descrizione                    |
|-------|--------------------------------|
| 0     | Estensione non specificata        |
| 1     | Didascalie normali                |
| 2     | Didascalie grandi                   |
| 3     | Didascalie degli elementi figlio            |
| 5     | Didascalie normali chiuse         |
| 6     | Didascalie grandi chiuse            |
| 7     | Didascalie chiuse degli elementi figlio     |
| 9     | Forced                         |
| 13    | Commenti del normale Director     |
| 14    | Commenti di Big Director        |
| 15    | Commenti del direttore per gli elementi figlio |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'estensione del linguaggio di sottoimmagine fornisce ulteriori informazioni sulla sottoimmagine.

 

 



