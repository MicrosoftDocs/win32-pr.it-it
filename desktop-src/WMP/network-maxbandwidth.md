---
title: Network.maxBandwidth
description: La proprietà maxBandwidth specifica o recupera la larghezza di banda massima consentita.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Network.maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c06c84762cd0d68af8af1cc9405036c5aecce317a61dbf292d3213bed351e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574147"
---
# <a name="networkmaxbandwidth"></a>Network.maxBandwidth

La **proprietà maxBandwidth** specifica o recupera la larghezza di banda massima consentita.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **maxBandwidth**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**long**).

## <a name="remarks"></a>Commenti

Nessun valore predefinito per questa proprietà. Il valore può essere specificato durante Windows Media Player riproduzione, ma la modifica non avrà effetto fino a quando l'elemento multimediale corrente non viene rilasciato aprendone un altro o chiamando *Player.* **Chiudere**. Windows Media Player tenta di ottenere la massima larghezza di banda possibile. Solo nel caso del valore impostato si verificherà una riduzione della larghezza di banda.

Questa impostazione è utile per ridurre la quantità di larghezza di banda usata, in particolare nel caso di un flusso MBR (Multiple Bit Rate). Un flusso MBR contiene più flussi con velocità in bit diverse. In alcuni casi, può essere preferibile usare un flusso con una velocità in bit inferiore a quella richiesta dal client. In questo caso, l'impostazione **della proprietà maxBandwidth** selezionerà un flusso a velocità in bit inferiore.

Ad esempio, un flusso MBR può includere flussi codificati a 20 kilobit al secondo (Kbps), 37 Kbps e 200 Kbps. L'impostazione della proprietà **maxBandwidth** su 50.000 (50 Kbps) selezionerà il flusso a 37 Kbps anziché il flusso di 200 Kbps.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Di rete**](network-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





