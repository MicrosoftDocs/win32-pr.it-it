---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfileId
description: Il metodo ConfigureFilterUsingProfileId configura il filtro per la scrittura di un file ASF con un indice dell'identificatore del profilo (ID) dall'elenco dei profili di sistema. (Solo per i profili Windows Media Format 4,0).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Metodo ConfigureFilterUsingProfileId Windows Media Format
- Metodo ConfigureFilterUsingProfileId Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299966"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Metodo IConfigAsfWriter:: ConfigureFilterUsingProfileId

Il metodo **ConfigureFilterUsingProfileId** configura il filtro per la scrittura di un file ASF con un indice dell'identificatore del profilo (ID) dall'elenco dei profili di sistema. (Solo per i profili Windows Media Format 4,0).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwProfileId* \[ in\]
</dt> <dd>

ID del profilo definito nella versione 4,0 di Windows Media Format SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                         | Descrizione                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Il metodo è riuscito.<br/>        |
| <dl> <dt>**E \_ non riescono**</dt> </dl>              | Profilo non valido.<br/>    |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl> | Il grafico del filtro è stato arrestato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo è ora obsoleto perché presuppone la versione 4,0 di profili SDK di formato Windows Media. Per configurare il filtro per i profili versione 7,0 e successive, usare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) o [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

