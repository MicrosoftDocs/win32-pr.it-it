---
title: Proprietà CounterItem. Color
description: Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Proprietà Color SysMon
- Proprietà Color SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741919"
---
# <a name="counteritemcolor-property"></a>Proprietà CounterItem. Color

Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valore proprietà

Colore utilizzato per rappresentare il valore del contatore.

## <a name="remarks"></a>Commenti

Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori. Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori. Per distinguere i contatori gli uni dagli altri, SYSMON modifica lo [**stile di linea**](counteritem-linestyle.md) usato per ogni multiplo di sedici contatori fino ai primi 80 contatori. Ad esempio, i primi sedici contatori utilizzano uno stile di linea a tinta unita, i successivi sedici utilizzano uno stile di linea tratteggiata e così via. SYSMON imposta quindi la [**lunghezza della riga**](counteritem-width.md) su 2 per i contatori 81-96 e su 3 per i contatori 96-112. Se la raccolta contiene più di 112 contatori, i contatori conterranno valori di colore, stile linea e larghezza duplicati.

**Prima di Windows Vista:** Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori. Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori. Per distinguere i contatori gli uni dagli altri, SYSMON aumenta la [**lunghezza della linea**](counteritem-width.md) dei primi tre contatori che ricevono la stessa assegnazione di colore. Se più di tre contatori utilizzano lo stesso colore, SYSMON sceglie in modo casuale la lunghezza della riga da utilizzare per il contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





