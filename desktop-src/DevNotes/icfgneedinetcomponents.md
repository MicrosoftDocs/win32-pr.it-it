---
description: Determina se i componenti contrassegnati nelle opzioni sono installati nel sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Funzione IcfgNeedInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 9b0d533e234986f54c6a4de668273bda08d9c810dc9f5a93acb3aaf030cea665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390661"
---
# <a name="icfgneedinetcomponents-function"></a>Funzione IcfgNeedInetComponents

Determina se i componenti contrassegnati nelle opzioni sono installati nel sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwfOptions* 
</dt> <dd>

Combinazione dei flag seguenti che specificano i componenti da rilevare dall'elenco seguente.



| Valore                                                                                                                                                                                                                                  | Significato                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ InstallMAIL**</dt> <dt>0x00000004</dt> </dl> | È Exchange o la posta Internet?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ InstallRAS**</dt> <dt>0x00000002</dt> </dl>    | Ras è necessario?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ InstallTCP**</dt> <dt>0x00000001</dt> </dl>    | TCP/IP è necessario?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

Se questo valore è diverso da **NULL,** viene restituito **TRUE** se uno o più componenti non sono installati nel sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Se non si verificano errori, restituisce il **codice ERROR \_ SUCCESS.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
