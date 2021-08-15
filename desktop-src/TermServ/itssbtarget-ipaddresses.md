---
title: Proprietà ITsSbTarget IpAddresses
description: Recupera o specifica gli indirizzi IP esterni della destinazione.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Proprietà TargetExternalIpAddresses Servizi Desktop remoto
- Proprietà TargetExternalIpAddresses Servizi Desktop remoto , interfaccia ITsSbTarget
- Proprietà TargetExternalIpAddresses Servizi Desktop remoto , interfaccia ITsSbTarget
- Proprietà IpAddresses Servizi Desktop remoto
- Proprietà IpAddresses Servizi Desktop remoto, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto proprietà , IpAddresses
- Proprietà IpAddresses Servizi Desktop remoto, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto proprietà IpAddresses
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ff06e60f125590154a17cb7467deae3611a617b684e9068439c9e15609d8fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351254"
---
# <a name="itssbtargetipaddresses-property"></a>Proprietà ITsSbTarget::IpAddresses

Recupera o specifica gli indirizzi IP esterni della destinazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una matrice [**di strutture \_ ConnectionPoint TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) che ricevono gli indirizzi IP esterni della destinazione.

Puntatore a una **variabile DWORD** che contiene il numero di indirizzi IP esterni nel *parametro sockaddr.* Se il numero di indirizzi è sconosciuto, passare *sockaddr* come **NULL.** Il metodo restituirà il numero di strutture [**\_ ConnectionPoint TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessarie per l'allocazione nella matrice a cui punta il *parametro sockaddr.*

## <a name="remarks"></a>Commenti

Questa proprietà era nota in precedenza come **TargetExternalIpAddresses** in Windows Server 2008 R2.

Se il numero di indirizzi IP esterni è sconosciuto, è possibile chiamare questo metodo con *sockaddr* impostato su **NULL.** Il metodo restituirà quindi, nel *parametro numAddresses,* il numero di strutture [**\_ ConnectionPoint TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessarie per ricevere tutti gli indirizzi IP esterni. Allocare la matrice per *sockaddr* in base a questo numero e quindi chiamare di nuovo il metodo , impostando *sockaddr* sulla matrice appena allocata e *numAddresses* sul numero restituito dalla prima chiamata.

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
<td>Idl<br/></td>
<td><dl> <dt>Sbtsv.idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget definito come:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 in Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**Punto di connessione \_ TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





