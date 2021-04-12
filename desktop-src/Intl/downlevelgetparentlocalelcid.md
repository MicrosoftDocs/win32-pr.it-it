---
description: Recupera l'identificatore delle impostazioni locali per l'elemento padre delle impostazioni locali specificate.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Funzione DownlevelGetParentLocaleLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348146"
---
# <a name="downlevelgetparentlocalelcid-function"></a>DownlevelGetParentLocaleLCID (funzione)

Recupera l' [identificatore delle impostazioni locali](locale-identifiers.md) per l'elemento padre delle impostazioni locali specificate.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede il pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintassi


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ in\]
</dt> <dd>

Identificatore delle impostazioni locali per il quale recuperare l'identificatore delle impostazioni locali padre. È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o usare uno dei valori predefiniti seguenti.

-   [impostazioni locali \_ INvariabili](locale-invariant.md)
-   [impostazioni locali del \_ sistema \_](locale-system-default.md)
-   [\_impostazione predefinita utente impostazioni locali \_](locale-user-default.md)

**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.

-   [impostazioni locali \_ personalizzate \_ predefinite](locale-custom-constants.md)
-   [\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_](locale-custom-constants.md)
-   [impostazioni locali \_ personalizzate non \_ specificate](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'identificatore delle impostazioni locali padre in caso di esito positivo; in caso contrario, 0. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore Microsoft NLS XPor Windows Vista<br/>     |
| Intestazione<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
