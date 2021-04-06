---
title: Proprietà TargetName di ITsSbTarget
description: Specifica o Recupera il nome della destinazione.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045919"
---
# <a name="itssbtargettargetname-property"></a>Proprietà ITsSbTarget:: TargetName

Specifica o Recupera il nome della destinazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Variabile **BSTR** che specifica il nome di destinazione.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura prima di Windows Server 2012.

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
<td>Windows Server 2012<br/></td>
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

 

 





