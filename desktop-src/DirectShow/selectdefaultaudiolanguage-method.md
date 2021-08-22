---
description: Il metodo SelectDefaultAudioLanguage imposta la lingua audio predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Metodo SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b649993cc3e110e78ba0a674e414dd4214af982dd44d64fcc1aca7646d1b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072625"
---
# <a name="selectdefaultaudiolanguage-method"></a>Metodo SelectDefaultAudioLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectDefaultAudioLanguage` metodo imposta la lingua audio predefinita corrente nell'oggetto MSWebDVD.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*Ilang*
</dt> <dd>

Specifica la lingua come valore Integer LCID.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Specifica l'estensione del linguaggio audio DVD come valore intero.



| Valore | Descrizione       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Sottotitoli          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



