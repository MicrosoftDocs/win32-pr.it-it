---
description: Verifica un singolo file di catalogo usando i criteri di firma del codice del sistema operativo standard, ad esempio la firma del driver.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325200"
---
# <a name="psetupverifycatalogfile-function"></a>pSetupVerifyCatalogFile (funzione)

\[Questa funzione non è più supportata da Microsoft. Per un file INF (installazione del dispositivo), gli sviluppatori devono usare **SetupVerifyInfFile**. Per convalidare un catalogo non basato su INF, usare **WinVerifyTrust**.\]

Verifica un singolo file di catalogo usando i criteri di firma del codice del sistema operativo standard, ad esempio la firma del driver.

## <a name="syntax"></a>Sintassi


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CatalogFullPath* \[ in\]
</dt> <dd>

Percorso completo del file di catalogo da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, viene restituito l' **errore \_ esito positivo**; in caso contrario, viene restituito l'errore da [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
