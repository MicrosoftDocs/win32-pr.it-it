---
title: Metodo SetProgramList della classe Win32_TSVirtualIP
description: Sovrascrive l'elenco dei programmi che usano la virtualizzazione IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Metodo SetProgramList Servizi Desktop remoto
- Metodo SetProgramList Servizi Desktop remoto , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Servizi Desktop remoto, metodo SetProgramList
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
ms.openlocfilehash: 22ac74ca1a718fe1ec3c561b70da935d00a15f1bcb040cb29464ed9b6e52195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349607"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Metodo SetProgramList della classe \_ Win32 TSVirtualIP

Sovrascrive l'elenco dei programmi che usano la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Elenco programmi* \[ Pollici\]
</dt> <dd>

Tipo: **\[ \] string**

Matrice di stringhe che contengono il percorso e i nomi file dei programmi che usano la virtualizzazione IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **unint32**

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

 

 





