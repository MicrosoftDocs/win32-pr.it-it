---
title: Metodo seprogrammer della classe Win32_TSVirtualIP
description: Sovrascrive l'elenco di programmi che usano la virtualizzazione IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Metodo seprogrammer Servizi Desktop remoto
- Metodo seprogramname Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo seprogramname
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518022"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Metodo seprogrammer della classe Win32 \_ TSVirtualIP

Sovrascrive l'elenco di programmi che usano la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Programmatore* \[ in\]
</dt> <dd>

Tipo: **stringa \[ \]**

Matrice di stringhe che contengono il percorso e i nomi file dei programmi che utilizzano la virtualizzazione IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **unint32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





