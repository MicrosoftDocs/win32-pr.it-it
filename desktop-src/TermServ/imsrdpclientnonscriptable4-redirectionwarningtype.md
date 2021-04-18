---
title: Proprietà RedirectionWarningType di IMsRdpClientNonScriptable4
description: Controlla la presenza e l'aspetto della finestra di dialogo che informa l'utente del reindirizzamento.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301888"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a>Proprietà IMsRdpClientNonScriptable4:: RedirectionWarningType

Controlla la presenza e l'aspetto della finestra di dialogo che informa l'utente del reindirizzamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il tipo della finestra di dialogo che informa l'utente del reindirizzamento.

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)


</dt> <dd>

La finestra di dialogo non è specifica del server di pubblicazione.

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)


</dt> <dd>

La finestra di dialogo è per i file non firmati.

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)


</dt> <dd>

La finestra di dialogo è destinata a un server di pubblicazione sconosciuto.

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)


</dt> <dd>

La finestra di dialogo è relativa ai file dell'utente.

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)


</dt> <dd>

La finestra di dialogo viene visualizzata per i file firmati con certificazione di terze parti.

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)


</dt> <dd>

La finestra di dialogo non viene visualizzata perché l'applicazione è pubblicata da un autore attendibile.

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)


</dt> <dd>

La finestra di dialogo non viene visualizzata perché l'applicazione è pubblicata da un autore attendibile.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Il valore **RedirectionWarningTypeDefault**, che corrisponde al valore predefinito di questa proprietà, non esercita alcun controllo sulla finestra di dialogo. In questo caso la proprietà di controllo è [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





