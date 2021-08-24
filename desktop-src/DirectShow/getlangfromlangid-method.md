---
description: Il metodo GetLangFromLangID recupera una stringa leggibile dall'utente quando viene specificato un ID lingua primario.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Metodo GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6041f12c82f0e659928db9f5aa02fd916d3ff9907bf3114eb40c525b8b1d8d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756751"
---
# <a name="getlangfromlangid-method"></a>Metodo GetLangFromLangID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo recupera una stringa leggibile quando viene `GetLangFromLangID` specificato un ID lingua primario.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Specifica l'ID della lingua primaria come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una rappresentazione di stringa della lingua che può essere visualizzata nell'interfaccia utente dell'applicazione.

## <a name="remarks"></a>Commenti

Anche se questo metodo è denominato , il parametro passato è in realtà `GetLangFromLangID` l'ID della lingua primaria, non l'ID lingua.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



