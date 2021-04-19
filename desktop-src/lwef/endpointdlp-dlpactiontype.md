---
description: Specifica il tipo di azione di un'operazione dlp (Data Loss Prevention) dell'endpoint.
title: Enumerazione DlpActionType (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495775"
---
# <a name="dlpactiontype-enumeration"></a>Enumerazione DlpActionType

Specifica il tipo di azione di un'operazione dlp (Data Loss Prevention) dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Costanti

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

Operazione di copia su supporti rimovibili.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

Operazione di copia in una cartella di rete condivisa.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

Operazione di copia negli Appunti.

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

Operazione di stampa.

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

Operazione di acquisizione dello schermo.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

Operazione eseguita da un'app non consentita.

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

Operazione destinata a una posizione cloud.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

Operazione che include l'accesso da parte di un'app Bluetooth.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

Operazione che include l'accesso da parte di un desktop remoto.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

Valore massimo dell'enumerazione.

</dd> </dl>
 

## <a name="remarks"></a>Commenti

I valori di questa enumerazione vengono usati dalla [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) struttura .

## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |

