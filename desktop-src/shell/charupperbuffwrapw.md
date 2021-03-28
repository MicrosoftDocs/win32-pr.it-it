---
description: Converte i caratteri minuscoli di un buffer in caratteri maiuscoli.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW (funzione)
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
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525398"
---
# <a name="charupperbuffwrapw-function"></a>CharUpperBuffWrapW (funzione)

\[**CharUpperBuffWrapW** è disponibile per l'utilizzo in Windows XP. Potrebbe non essere disponibile nelle versioni successive. È consigliabile usare [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) al suo posto.\]

Converte i caratteri minuscoli di un buffer in caratteri maiuscoli. La funzione converte i caratteri sul posto.

> [!Note]  
> **CharUpperBuffWrapW** è un wrapper per la funzione **CharUpperBuffW** . Per ulteriori note sull'utilizzo, vedere la pagina [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .

 

## <a name="syntax"></a>Sintassi


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PCH* \[ in\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a un buffer che contiene uno o più caratteri Unicode da elaborare.

</dd> <dt>

*cchLength* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Specifica la dimensione, in caratteri, del buffer a cui punta *PCH*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Numero di caratteri elaborati.

## <a name="remarks"></a>Commenti

Il metodo preferito consiste nell'usare [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) insieme a Microsoft Layer for Unicode (MSLU).

**CharUpperBuffWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 44.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
