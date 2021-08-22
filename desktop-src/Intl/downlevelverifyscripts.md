---
description: Confronta due elenchi enumerati di script.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Funzione DownlevelVerifyScripts (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: df0bdb1e8968d6bb044a3f270eb9200adf1ecaa54137fe3cface0e0898a9b5be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068241"
---
# <a name="downlevelverifyscripts-function"></a>Funzione DownlevelVerifyScripts

Confronta due elenchi enumerati di script.

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. L'uso richiede il pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

## <a name="syntax"></a>Sintassi


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni di verifica dello script.



| Valore                                                                                                                                                             | Significato                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ ALLOW \_ LATIN**</dt> </dl> | Consentire "Latn" (alfabeto latino) nell'elenco di test, anche se non è presente nell'elenco delle impostazioni locali.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ Pollici\]
</dt> <dd>

Puntatore all'elenco delle impostazioni locali, l'elenco enumerato di script per le impostazioni locali specificate. Questo elenco viene in genere popolato chiamando [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).

</dd> <dt>

*cchLocaleScripts* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, della stringa indicata da *lpLocaleScripts*. L'applicazione imposta questo parametro su -1 se la stringa ha terminazione Null. Se questo parametro è impostato su 0, la funzione ha esito negativo.

</dd> <dt>

*lpTestScripts* \[ Pollici\]
</dt> <dd>

Puntatore all'elenco di test, un secondo elenco enumerato di script. Questo elenco viene in genere popolato chiamando [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).

</dd> <dt>

*cchTestScripts* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, della stringa indicata da *lpTestScripts*. L'applicazione imposta questo parametro su -1 se la stringa ha terminazione Null. Se questo parametro è impostato su 0, la funzione ha esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'elenco di test è non vuoto e tutti gli elementi nell'elenco sono inclusi anche nell'elenco delle impostazioni locali. In caso contrario, la funzione restituisce **FALSE.**

Il valore restituito **FALSE** può indicare che l'elenco di test contiene un elemento non presente nell'elenco delle impostazioni locali oppure può indicare un errore. Per distinguere tra questi due casi, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **DownlevelVerifyScripts** ha determinato che nell'elenco di test è presente un elemento non presente nell'elenco delle impostazioni locali, **GetLastError** restituisce ERROR \_ SUCCESS. In caso contrario, **GetLastError** può restituire uno dei codici di errore seguenti:

-   ERRORE \_ FLAG NON \_ VALIDI. I valori forniti per i flag non sono validi.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

Questa funzione confronta le stringhe, ad esempio "Latn; Cyrl;", costituito da una serie di nomi di script di 4 caratteri, con ogni nome di script seguito da un punto e virgola. Ha anche un caso speciale per il fatto che lo script latino viene spesso usato nelle lingue e nelle impostazioni locali per cui non è nativo.

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi di dominio [internazionalizzati (IDN).](handling-internationalized-domain-names--idns.md)

Di seguito sono riportati esempi di restituzione di questa funzione e di una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in diversi scenari. Gli ultimi due esempi illustrano, rispettivamente, un caso in cui l'elenco di test non contiene un punto e virgola di terminazione (stringa in formato non valido) e un caso in cui l'elenco di test è vuoto.



| Stringa "Locale" | Stringa "Test" | *dwFlags*        | Valore restituito | GetLastError restituito       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana; | Hani;         | N/A              | **TRUE**     | N/A                       |
| Hani; Hira; Kana; | Hani; Latn;    | 0                | **FALSE**    | ERRORE \_ RIUSCITO            |
| Hani; Hira; Kana; | Hani; Latn;    | VS \_ ALLOW \_ LATIN | **TRUE**     | N/A                       |
| Hani; Hira; Kana; | Cyrl;         | N/A              | **FALSE**    | ERRORE \_ RIUSCITO            |
| Hani; Hira; Kana; | Cyrl;         | N/A              | **FALSE**    | ERRORE \_ PARAMETRO NON \_ VALIDO |
| Hani; Hira; Kana; |               | N/A              | **FALSE**    | ERRORE \_ RIUSCITO            |



 

Il file di intestazione e la DLL necessari fanno parte del download ["MICROSOFT Internationalized Domain Name (IDN) Mitigation APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) disponibile nell'Area [download MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                         |
| Componente ridistribuibile<br/>          | API di mitigazione idn (Internationalized Domain Name) di Microsoft in Windows XP con SP2,Windows Server 2003 con SP1 o Windows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
