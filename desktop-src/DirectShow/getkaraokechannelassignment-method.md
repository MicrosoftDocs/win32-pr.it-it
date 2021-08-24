---
description: Il metodo GetKaraokeChannelAssignment recupera un valore che indica come vengono assegnati i canali per il distacco ai parlanti.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Metodo GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812551"
---
# <a name="getkaraokechannelassignment-method"></a>Metodo GetKaraokeChannelAssignment

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo recupera un valore che indica la modalità di assegnazione dei `GetKaraokeChannelAssignment` canali di disasuasore agli altoparlanti.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il flusso audio come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un intero che indica l'assegnazione del parlante per il flusso specificato.



| Codice restituito | Descrizione                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Il flusso viene assegnato agli altoparlanti sinistro e destro.                  |
| 3           | Il flusso viene assegnato agli altoparlanti sinistro, destro e centrale.         |
| 4           | Il flusso viene assegnato agli altoparlanti sinistro, destro e audio1.         |
| 5           | Il flusso viene assegnato agli altoparlanti sinistro, destro, centrale e audio1. |
| 6           | Il flusso viene assegnato agli altoparlanti sinistro, destro e audio2.         |
| 7           | Il flusso viene assegnato agli altoparlanti sinistro, destro, centrale e audio2. |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



