---
title: Proprietà IMsTscNonScriptable ClearTextPassword
description: Imposta la password Desktop remoto ActiveX controllo di accesso in formato testo non crittografato.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Proprietà ClearTextPassword Servizi Desktop remoto
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà , ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà , ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà , ClearTextPassword
- Proprietà ClearTextPassword Servizi Desktop remoto , oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà , ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125051"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Proprietà IMsTscNonScriptable::ClearTextPassword

Imposta la password Desktop remoto ActiveX controllo di accesso in formato testo non crittografato.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valore proprietà

Password da utilizzare per la connessione, specificata in formato testo non crittografato.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

La password viene passata al server nel canale di comunicazione RDP crittografato in modo sicuro. Dopo aver impostato una password in testo non crittografato, non è possibile recuperarla in formato testo non crittografato.

La **proprietà ClearTextPassword** può essere impostata solo quando Desktop remoto ActiveX controllo non si trova nello stato connesso. L'impostazione di questa proprietà non riesce se il controllo è connesso. Per verificare lo stato connesso, recuperare la [**proprietà IMsTscAx::Connected.**](imstscax-connected.md)

È anche possibile chiamare questo metodo per impostare una password in testo non crittografato prima di convertirla in una password con codifica portabile o in una password con codifica binaria (non portabile). Si noti tuttavia che le password codificate non devono essere considerate crittografate in modo sicuro.

Se si chiama prima questo metodo per impostare una password in formato testo non crittografato, è possibile convertire la password in formato codificato.

**Per convertire una password in testo non crittografato in formato codificato**

1.  Impostare la password in formato testo non crittografato nella **proprietà ClearTextPassword.**
2.  Per recuperare la password in formato binario (non portabile), recuperare le [**proprietà BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt.**](imstscnonscriptable-binarysalt.md) Sia la parte della password codificata che la parte salt sono necessarie per impostare una password in formato codificato binario.
3.  Per recuperare la password in formato con codifica portabile, recuperare il [**metodo PortablePassword**](imstscnonscriptable-portablepassword.md) e le [**proprietà PortableSalt.**](imstscnonscriptable-portablesalt.md) Entrambe le parti sono necessarie per impostare una password in formato con codifica portabile.

Dopo aver seguito i tre passaggi precedenti, è possibile impostare la password in formato codificato impostando le proprietà [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) o [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt.**](imstscnonscriptable-portablesalt.md) Entrambe le parti sono obbligatorie.

Per abilitare l'accesso automatico, è necessario impostare anche le [**proprietà UserName**](imstscax-username.md) [**e Domain.**](imstscax-domain.md) Se la password non riesce ad autenticare l'utente, nel server viene visualizzata la finestra di dialogo Windows Accesso remoto per richiedere la password all'utente.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable è definito come c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





