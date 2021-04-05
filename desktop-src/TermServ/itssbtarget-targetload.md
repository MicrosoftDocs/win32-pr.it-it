---
title: Proprietà TargetLoad di ITsSbTarget
description: Recupera il carico relativo in una destinazione.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetLoad
- Servizi Desktop remoto proprietà TargetLoad, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà TargetLoad
- Servizi Desktop remoto proprietà TargetLoad, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà TargetLoad
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
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718583"
---
# <a name="itssbtargettargetload-property"></a>Proprietà ITsSbTarget:: TargetLoad

Recupera il carico relativo in una destinazione. Questo valore è basato sul numero di sessioni esistenti e in sospeso. Per impostazione predefinita, una sessione in sospeso ha lo stesso valore di una sessione esistente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valore proprietà

Numero che rappresenta il carico relativo in una destinazione.

## <a name="remarks"></a>Commenti

Il peso di una sessione in sospeso relativa a una sessione attiva può essere modificato impostando il valore del parametro *lb \_ ConnectionEstablishmentPenalty* per il gestore connessione. Questo parametro si trova nella chiave del registro di **\\ sistema HKLM System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** . Il valore predefinito 1 indica che le sessioni in sospeso hanno lo stesso peso delle sessioni attive.

Questa proprietà è disponibile in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato nell'interfaccia [**ITsSbTargetEx**](itssbtargetex.md) .

## <a name="requirements"></a>Requisiti



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Client minimo supportato<br/></td>
<td>Nessuno supportato<br/></td>
</tr>
<tr class="even">
<td>Server minimo supportato<br/></td>
<td>Windows Server 2016<br/></td>
</tr>
<tr class="odd">
<td>IDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget viene definito come segue:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-B456-5fd5840901c0 in Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





