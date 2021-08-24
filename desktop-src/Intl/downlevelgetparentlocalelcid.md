---
description: Recupera l'identificatore delle impostazioni locali per l'elemento padre delle impostazioni locali specificate.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Funzione DownlevelGetParentLocaleLCID (Nlsdl.h)
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
ms.openlocfilehash: 64cefdf4cc2a2c522a8295ab44e1810f0364d706d378979637700a7a3b72343a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765441"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Funzione DownlevelGetParentLocaleLCID

Recupera l'identificatore [delle impostazioni](locale-identifiers.md) locali per l'elemento padre delle impostazioni locali specificate.

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. L'uso richiede il pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [LOCALE \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintassi


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ Pollici\]
</dt> <dd>

Identificatore delle impostazioni locali delle impostazioni locali per cui recuperare l'identificatore delle impostazioni locali padre. È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o uno dei valori predefiniti seguenti.

-   [\_INVARIANTE DELLE IMPOSTAZIONI LOCALI](locale-invariant.md)
-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE DEL \_ SISTEMA](locale-system-default.md)
-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE \_ DELL'UTENTE](locale-user-default.md)

**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.

-   [IMPOSTAZIONI \_ LOCALI PERSONALIZZATE \_ PREDEFINITE](locale-custom-constants.md)
-   [IMPOSTAZIONE PREDEFINITA \_ \_ DELL'INTERFACCIA \_ UTENTE PERSONALIZZATA DELLE IMPOSTAZIONI LOCALI](locale-custom-constants.md)
-   [IMPOSTAZIONI \_ LOCALI PERSONALIZZATE NON \_ SPECIFICATE](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'identificatore delle impostazioni locali padre in caso di esito positivo oppure 0 in caso contrario. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

Il file di intestazione e la DLL necessari fanno parte del download "Microsoft NLS Downlevel Data Mapping APIs", disponibile [nell'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore di Microsoft NLS in Windows XPor Windows Vista<br/>     |
| Intestazione<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
