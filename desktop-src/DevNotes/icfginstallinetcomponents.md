---
description: Installa i componenti di sistema specificati.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Funzione IcfgInstallInetComponents
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
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827257"
---
# <a name="icfginstallinetcomponents-function"></a>Funzione IcfgInstallInetComponents

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
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ InstallMAIL**</dt> <dt>0x00000004</dt> </dl> | Installare Exchange e la posta Internet.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ InstallRAS**</dt> <dt>0x00000002</dt> </dl>    | Installare RAS (se necessario).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Installare TCP/IP (se necessario).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Se questo valore è diverso da **NULL,** in caso di restituzione sarà **TRUE** solo se Windows necessario riavviare per completare l'installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Se non si verificano errori, restituisce il **codice ERROR \_ SUCCESS.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
