---
description: Il metodo SelectDefaultAudioLanguage imposta la lingua audio predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Metodo SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521274"
---
# <a name="selectdefaultaudiolanguage-method"></a>Metodo SelectDefaultAudioLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectDefaultAudioLanguage` metodo imposta la lingua audio predefinita corrente nell'oggetto mswebdvd.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Specifica la lingua come valore LCID di tipo Integer.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Specifica l'estensione di lingua audio DVD come valore intero.



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

 

 



