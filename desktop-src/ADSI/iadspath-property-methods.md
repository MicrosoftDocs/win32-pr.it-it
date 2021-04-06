---
title: Metodi di proprietà IADsPath (IADs. h)
description: Il metodo Property dell'interfaccia IADsPath imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPath ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742682"
---
# <a name="iadspath-property-methods"></a>Metodi di proprietà IADsPath

Il metodo Property dell'interfaccia [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Percorso**
</dt> <dd> <dl>

Percorso di una directory del file system.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**Tipo**
</dt> <dd> <dl>

Tipo di file del file system.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

**NomeVolume**
</dt> <dd> <dl>

Nome di un volume esistente del file system.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPath è definito come B287FCD5-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[**\_percorso annunci**](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





