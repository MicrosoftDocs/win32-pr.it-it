---
description: Confronta due elenchi enumerati di script.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Funzione DownlevelVerifyScripts (idndl. h)
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
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317160"
---
# <a name="downlevelverifyscripts-function"></a>DownlevelVerifyScripts (funzione)

Confronta due elenchi enumerati di script.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede il pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

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

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni di verifica dello script.



| Valore                                                                                                                                                             | Significato                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ consente il \_ latino**</dt> </dl> | Consenti "Latn" (alfabeto latino) nell'elenco dei test, anche se non è presente nell'elenco delle impostazioni locali.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ in\]
</dt> <dd>

Puntatore all'elenco delle impostazioni locali, l'elenco enumerato di script per le impostazioni locali specificate. Questo elenco viene popolato in genere chiamando [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).

</dd> <dt>

*cchLocaleScripts* \[ in\]
</dt> <dd>

Dimensione, in caratteri, della stringa indicata da *lpLocaleScripts*. L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null. Se questo parametro è impostato su 0, la funzione avrà esito negativo.

</dd> <dt>

*lpTestScripts* \[ in\]
</dt> <dd>

Puntatore all'elenco dei test, un secondo elenco enumerato di script. Questo elenco viene popolato in genere chiamando [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).

</dd> <dt>

*cchTestScripts* \[ in\]
</dt> <dd>

Dimensione, in caratteri, della stringa indicata da *lpTestScripts*. L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null. Se questo parametro è impostato su 0, la funzione avrà esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'elenco di test non è vuoto e tutti gli elementi dell'elenco sono inclusi anche nell'elenco delle impostazioni locali. In caso contrario, la funzione restituisce **false**.

Un valore restituito di **false** può indicare che l'elenco di test contiene un elemento che non è presente nell'elenco delle impostazioni locali oppure può indicare un errore. Per distinguere tra questi due casi, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **DownlevelVerifyScripts** ha determinato che è presente un elemento nell'elenco di test che non è presente nell'elenco delle impostazioni locali, **GetLastError** restituisce Error \_ Success. In caso contrario, **GetLastError** può restituire uno dei codici di errore seguenti:

-   flag di errore \_ non validi \_ . I valori specificati per i flag non sono validi.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

Questa funzione Confronta le stringhe, ad esempio "Latn; Cyrl; ", costituito da una serie di nomi di script di 4 caratteri, con ogni nome di script seguito da un punto e virgola. Ha anche un caso speciale per tenere conto del fatto che lo script latino viene spesso usato in linguaggi e impostazioni locali per cui non è nativo.

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).

Di seguito sono riportati esempi della restituzione di questa funzione e di una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in diversi scenari. Gli ultimi due esempi illustrano, rispettivamente, un caso in cui l'elenco di test non dispone di un punto e virgola di terminazione (stringa in formato non corretto) e di un caso in cui l'elenco di test è vuoto.



| Stringa "impostazioni locali" | Stringa "test" | *dwFlags*        | Valore restituito | Restituito GetLastError       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani Hira Kana | Hani         | N/D              | **TRUE**     | N/D                       |
| Hani Hira Kana | Hani Latn    | 0                | **FALSE**    | ERRORE \_ riuscito            |
| Hani Hira Kana | Hani Latn    | VS \_ consente il \_ latino | **TRUE**     | N/D                       |
| Hani Hira Kana | Cyrl         | N/D              | **FALSE**    | ERRORE \_ riuscito            |
| Hani Hira Kana | Cyrl         | N/D              | **FALSE**    | ERRORE \_ parametro non valido \_ |
| Hani Hira Kana |               | N/D              | **FALSE**    | ERRORE \_ riuscito            |



 

Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                         |
| Componente ridistribuibile<br/>          | API di mitigazione Microsoft per il nome di dominio internazionale (IDN) in Windows XP con SP2, Windows Server 2003 con SP1, Windows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
