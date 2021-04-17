---
description: Il metodo GetDVDTextLanguageLCID recupera l'identificatore delle impostazioni locali (LCID) per il blocco di stringhe di testo specificato.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Metodo GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520633"
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

Specifica il blocco di lingua del testo nel disco come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore LCID che contiene informazioni che specificano la lingua in cui vengono scritte le stringhe.

## <a name="remarks"></a>Commenti

Le stringhe di testo aggiuntive vengono archiviate in blocchi contigui sul disco. Ogni lingua ha un blocco di stringhe. Un'applicazione specifica questi blocchi in base a un indice, che deve essere minore del valore restituito da [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



