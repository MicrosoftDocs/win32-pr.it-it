---
description: Converte i caratteri minuscoli in un buffer in caratteri maiuscoli.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Funzione CharUpperBuffWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861556"
---
# <a name="charupperbuffwrapw-function"></a>Funzione CharUpperBuffWrapW

\[**CharUpperBuffWrapW** è disponibile per l'uso in Windows XP. Potrebbe non essere disponibile nelle versioni successive. È consigliabile [**usare CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) al suo posto.\]

Converte i caratteri minuscoli in un buffer in caratteri maiuscoli. La funzione converte i caratteri sul posto.

> [!Note]  
> **CharUpperBuffWrapW** è un wrapper per la **funzione CharUpperBuffW.** Per altre note sull'utilizzo, vedere la pagina [**CharUpperBuff.**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)

 

## <a name="syntax"></a>Sintassi


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pch* \[ Pollici\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a un buffer che contiene uno o più caratteri Unicode da elaborare.

</dd> <dt>

*cchLength* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Specifica le dimensioni, in caratteri, del buffer a cui punta *pch*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Numero di caratteri elaborati.

## <a name="remarks"></a>Commenti

Il metodo preferito è usare [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) insieme al livello Microsoft per Unicode (MSLU).

**CharUpperBuffWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando l'ordinale 44.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
