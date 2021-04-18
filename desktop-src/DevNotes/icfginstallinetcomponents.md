---
description: Installa i componenti di sistema specificati.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327677"
---
# <a name="icfginstallinetcomponents-function"></a>IcfgInstallInetComponents (funzione)

Installa i componenti di sistema specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle per la finestra padre.

</dd> <dt>

*dwfOptions* 
</dt> <dd>

Combinazione dei flag seguenti che controllano l'installazione e la configurazione.



| Valore                                                                                                                                                                                                                                  | Significato                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000004</dt> INSTALLMAIL </dl> | Installare Exchange e Internet mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000002</dt> INSTALLRAS </dl>    | Installare RAS (se necessario).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000001</dt> INSTALLTCP </dl>    | Installare TCP/IP (se necessario).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Se questo valore è diverso da **null**, in caso di restituzione sarà **true** solo se è necessario riavviare Windows per completare l'installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Se non si verificano errori, viene restituito il codice di **\_ esito positivo dell'errore** .

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
