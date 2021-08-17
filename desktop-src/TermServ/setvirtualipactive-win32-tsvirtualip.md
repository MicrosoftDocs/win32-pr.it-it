---
title: Metodo SetVirtualIPActive della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Metodo SetVirtualIPActive Servizi Desktop remoto
- Metodo SetVirtualIPActive Servizi Desktop remoto , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Servizi Desktop remoto , metodo SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab43a007a2a8b04e91d5225e648d5667a87c468cbd52c005d85f4ba6496c919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850920"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Metodo SetVirtualIPActive della classe \_ Win32 TSVirtualIP

Imposta il **valore della proprietà VirtualIPActive.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualIPActive* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Specifica se la virtualizzazione IP è attiva nel server. Può essere uno dei valori seguenti.

<dt>

zero
</dt> <dd>

La virtualizzazione IP non è attiva.

</dd> <dt>

diverso da zero
</dt> <dd>

La virtualizzazione IP è attiva.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





