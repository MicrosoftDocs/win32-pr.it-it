---
description: Determina se i componenti contrassegnati nelle opzioni sono installati nel sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents (funzione)
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
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330966"
---
# <a name="icfgneedinetcomponents-function"></a>IcfgNeedInetComponents (funzione)

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
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000004</dt> INSTALLMAIL </dl> | Exchange o Internet mail è necessario?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000002</dt> INSTALLRAS </dl>    | RAS è necessario?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_**</dt> <dt>0x00000001</dt> INSTALLTCP </dl>    | TCP/IP è necessario?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

Se questo valore è diverso da **null**, viene restituito **true** se uno o più componenti non sono installati nel sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Se non si verificano errori, viene restituito il codice di **\_ esito positivo dell'errore** .

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
