---
title: Proprietà TargetLoad ITsSbTarget
description: Recupera il carico relativo su una destinazione.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Proprietà TargetLoad Servizi Desktop remoto
- Proprietà TargetLoad Servizi Desktop remoto, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto , proprietà TargetLoad
- Proprietà TargetLoad Servizi Desktop remoto, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto , proprietà TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d6d4839f60ef4b4af33498658bd78bf234c14f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482347"
---
# <a name="itssbtargettargetload-property"></a>Proprietà ITsSbTarget::TargetLoad

Recupera il carico relativo su una destinazione. Questo valore è basato sul numero di sessioni esistenti e in sospeso. Per impostazione predefinita, una sessione in sospeso ha lo stesso valore di una sessione esistente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valore proprietà

Numero che rappresenta il carico relativo su una destinazione.

## <a name="remarks"></a>Commenti

Il peso di una sessione in sospeso rispetto a una sessione attiva può essere modificato impostando il valore del parametro *\_ LB ConnectionEstablishmentPenalty* per Gestore connessione. Questo parametro si trova nella chiave del Registro di sistema **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** Il valore predefinito 1 specifica che le sessioni in sospeso hanno lo stesso peso delle sessioni attive.

Questa proprietà è disponibile in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato [**nell'interfaccia ITsSbTargetEx.**](itssbtargetex.md)

## <a name="requirements"></a>Requisiti




| | | Client minimo supportato<br /> | Nessuno supportato<br /> | | Server minimo supportato<br /> | Windows Server 2016<br /> | | IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | | IID<br /> | IID_ITsSbTarget è definito come:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 in Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





