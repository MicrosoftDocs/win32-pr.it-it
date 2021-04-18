---
title: Rete. maxBandwidth
description: La proprietà maxBandwidth specifica o recupera la larghezza di banda massima consentita.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Media Player di Windows Network. maxBandwidth
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
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324381"
---
# <a name="networkmaxbandwidth"></a>Rete. maxBandwidth

La proprietà **maxBandwidth** specifica o recupera la larghezza di banda massima consentita.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **maxBandwidth**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Long**).

## <a name="remarks"></a>Commenti

Nessun valore predefinito per questa proprietà. Il valore può essere specificato durante la riproduzione di Windows Media Player, ma la modifica non verrà applicata fino a quando l'elemento multimediale corrente non viene rilasciato aprendone un altro o chiamando *Player*. **Chiudi**. Windows Media Player tenta di ottenere la massima larghezza di banda possibile. Solo nel caso del valore impostato, si verificherà una riduzione della larghezza di banda.

Questa impostazione è utile per ridurre la quantità di larghezza di banda usata, in particolare nel caso di un flusso a più velocità in bit (MBR). Un flusso MBR contiene più flussi con velocità in bit diverse. In alcuni casi, può essere utile usare un flusso con una velocità in bit inferiore a quella richiesta dal client. In questo caso, l'impostazione della proprietà **maxBandwidth** consente di selezionare un flusso a velocità in bit inferiore.

Ad esempio, un flusso MBR può includere flussi codificati a 20 kilobit al secondo (Kbps), 37 kbps e 200 Kbps. Se si imposta la proprietà **maxBandwidth** su 50.000 (50 Kbps), si selezionerà il flusso 37 Kbps anziché il flusso da 200 Kbps.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





