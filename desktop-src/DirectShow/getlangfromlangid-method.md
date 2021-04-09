---
description: Il metodo GetLangFromLangID recupera una stringa leggibile quando viene specificato un ID di lingua primario.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Metodo GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876542"
---
# <a name="getlangfromlangid-method"></a>Metodo GetLangFromLangID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetLangFromLangID` metodo recupera una stringa leggibile quando viene specificato un ID di lingua primario.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Specifica l'ID della lingua primaria come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una rappresentazione di stringa del linguaggio che può essere visualizzato nell'interfaccia utente dell'applicazione.

## <a name="remarks"></a>Commenti

Sebbene questo metodo sia denominato `GetLangFromLangID` , il parametro passato è in realtà l'ID della lingua primaria, non l'ID della lingua.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



