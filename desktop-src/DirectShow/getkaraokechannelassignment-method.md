---
description: Il metodo GetKaraokeChannelAssignment recupera un valore che indica la modalità di assegnazione dei canali karaoke agli altoparlanti.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Metodo GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877105"
---
# <a name="getkaraokechannelassignment-method"></a>Metodo GetKaraokeChannelAssignment

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetKaraokeChannelAssignment` metodo recupera un valore che indica la modalità di assegnazione dei canali karaoke ai relatori.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Specifica il flusso audio come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer che indica l'assegnazione del altoparlante per il flusso specificato.



| Codice restituito | Descrizione                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Il flusso viene assegnato agli altoparlanti sinistro e destro.                  |
| 3           | Il flusso viene assegnato agli altoparlanti sinistro, destro e intermedio.         |
| 4           | Il flusso viene assegnato ai relatori Left, Right e AUDIO1.         |
| 5           | Il flusso viene assegnato agli altoparlanti a sinistra, a destra, al centro e a AUDIO1. |
| 6           | Il flusso viene assegnato ai relatori Left, Right e AUDIO2.         |
| 7           | Il flusso viene assegnato agli altoparlanti a sinistra, a destra, al centro e a AUDIO2. |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



