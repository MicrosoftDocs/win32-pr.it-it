---
title: Proprietà IconFile di IMsTscAdvancedSettings
description: Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà IconFile
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741506"
---
# <a name="imstscadvancedsettingsiconfile-property"></a>Proprietà IMsTscAdvancedSettings:: IconFile

Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.

> [!Note]  
> Questa proprietà non è supportata nel controllo ActiveX (MsRdp. ocx). È supportato nella libreria MsTscAx.dll inclusa nel client standard (MsTsc.exe).

 

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a>Valore proprietà

Percorso completo del file icona o di un file contenente i dati delle icone, ad esempio una DLL.

## <a name="error-codes"></a>Codici di errore

Restituisce un valore **\_ false**.

## <a name="remarks"></a>Commenti

L'estensione del nome file di un file icona è ". ico".

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





