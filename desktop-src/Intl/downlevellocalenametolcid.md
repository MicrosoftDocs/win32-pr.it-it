---
description: Converte un nome delle impostazioni locali in un identificatore delle impostazioni locali che può essere utilizzato per ottenere informazioni dal sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Funzione DownlevelLocaleNameToLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317159"
---
# <a name="downlevellocalenametolcid-function"></a>DownlevelLocaleNameToLCID (funzione)

Converte un [nome delle impostazioni locali](locale-names.md) in un [identificatore delle impostazioni locali](locale-identifiers.md) che può essere utilizzato per ottenere informazioni dal sistema operativo.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede un pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) per recuperare un identificatore delle impostazioni locali.

 

## <a name="syntax"></a>Sintassi


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il [nome delle impostazioni locali](locale-names.md).

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano il tipo di nome. Il valore predefinito è il \_ nome delle impostazioni locali di livello inferiore \_ .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'identificatore delle impostazioni locali che corrisponde al nome delle impostazioni locali in caso di esito positivo.

Se l'operazione non riesce, la funzione restituisce 0. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   flag di errore \_ non validi \_ . I valori specificati per i flag non sono validi.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa funzione non supporta le impostazioni locali non associate ad alcun paese. La funzione [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente supporta [impostazioni locali personalizzate](custom-locales.md), ma solo per Windows Vista e versioni successive.

 

Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e laterorWindows vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
