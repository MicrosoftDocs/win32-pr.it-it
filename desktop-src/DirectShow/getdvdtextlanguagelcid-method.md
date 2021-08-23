---
description: Il metodo GetDVDTextLanguageLCID recupera l'identificatore delle impostazioni locali (LCID) per il blocco di stringhe di testo specificato.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Metodo GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c60abedc3a986bfec766cc14c2251d9bed83650ee737762a4e870af9d283a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748721"
---
# <a name="getdvdtextlanguagelcid-method"></a>Metodo GetDVDTextLanguageLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetDVDTextLanguageLCID` metodo recupera l'identificatore delle impostazioni locali (LCID) per il blocco di stringhe di testo specificato.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Specifica il blocco di linguaggio di testo sul disco come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore LCID che contiene informazioni che specificano la lingua in cui vengono scritte le stringhe.

## <a name="remarks"></a>Commenti

Le stringhe di testo supplementari vengono archiviate in blocchi contigui sul disco. Ogni linguaggio ha un blocco di stringhe. Un'applicazione specifica questi blocchi in base a un indice, che deve essere minore del valore restituito da [**GetDVDTextNumberOfLanguages.**](getdvdtextnumberoflanguages-method.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



