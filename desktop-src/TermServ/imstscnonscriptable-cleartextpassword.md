---
title: Proprietà ClearTextPassword di IMsTscNonScriptable
description: Imposta la password del controllo ActiveX Desktop remoto in formato testo non crittografato.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà ClearTextPassword
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
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743527"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Proprietà IMsTscNonScriptable:: ClearTextPassword

Imposta la password del controllo ActiveX Desktop remoto in formato testo non crittografato.

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

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

La password viene passata al server nel canale di comunicazione RDP crittografato in modo sicuro. Dopo aver impostato una password in testo non crittografato, non è possibile recuperarla in formato testo non crittografato.

La proprietà **ClearTextPassword** può essere impostata solo quando il controllo ActiveX Desktop remoto non è nello stato connesso. L'impostazione di questa proprietà ha esito negativo se il controllo è connesso. Per verificare lo stato connesso, recuperare la proprietà [**IMsTscAx:: Connected**](imstscax-connected.md) .

È anche possibile chiamare questo metodo per impostare una password in testo non crittografato prima di convertirla in una password con codifica portatile o in una password con codifica binaria (non portabile). Si noti tuttavia che le password codificate non devono essere considerate crittografate in modo sicuro.

Se si chiama per la prima volta questo metodo per impostare una password in formato testo non crittografato, è possibile convertire la password in formato codificato.

**Per convertire una password in testo non crittografato nel formato codificato**

1.  Impostare la password in formato testo non crittografato nella proprietà **ClearTextPassword** .
2.  Per recuperare la password in formato binario (non portabile), recuperare la proprietà [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e le proprietà [**BinarySalt**](imstscnonscriptable-binarysalt.md) . Sia la parte della password codificata che la parte Salt sono necessarie per impostare una password in formato con codifica binaria.
3.  Per recuperare la password in formato con codifica portatile, recuperare il metodo [**PortablePassword**](imstscnonscriptable-portablepassword.md) e le proprietà [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Entrambe le parti sono necessarie per impostare una password in formato con codifica portatile.

Dopo aver seguito i tre passaggi precedenti, è possibile impostare la password in formato codificato impostando le proprietà [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) o [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Entrambe le parti sono obbligatorie.

Per abilitare l'accesso automatico, è necessario impostare anche il [**nome utente**](imstscax-username.md) e le proprietà del [**dominio**](imstscax-domain.md) . Se la password non è in grado di autenticare l'utente, la finestra di dialogo di accesso di Windows viene visualizzata sul server per richiedere la password all'utente.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e<br/> |



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

 

 





