---
description: Fornisce un elenco di script utilizzati nella stringa Unicode specificata.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Funzione DownlevelGetStringScripts (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 23eca82d97ac1da2d0f179c6e670ed032a57410490dcc5a52cf3005d75d65b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041621"
---
# <a name="downlevelgetstringscripts-function"></a>Funzione DownlevelGetStringScripts

Fornisce un elenco di script utilizzati nella stringa Unicode specificata.

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. L'uso richiede il pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).

 

## <a name="syntax"></a>Sintassi


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni per il recupero dello script.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ CONSENTE \_ L'EREDITARIETÀ \_ COMUNE**</dt> </dl> | Recuperare le informazioni sugli script "Qaii" (INHERITED) e "Zyyy" (COMMON). Questo valore non influisce sull'elaborazione di caratteri non assegnati. Questi caratteri nella stringa di input determinano sempre la visualizzazione di "Zzzz" (script UNASSIGNED) nella stringa di script.<br/> |



 

> [!Note]  
> Per impostazione predefinita, questa funzione ignora tutti i caratteri ereditati o comuni nella stringa Unicode di input. Se GSS ALLOW INHERITED COMMON non è impostato, né \_ \_ "Qaii" né "Zyyy" verranno visualizzati nella stringa di script, anche se la stringa di input contiene \_ tali caratteri. Se gSS ALLOW INHERITED COMMON è impostato e se la stringa di input contiene caratteri \_ \_ \_ ereditati e/o comuni, "Qaii" e/o "Zyyy" vengono visualizzati nella stringa di script. Vedere la sezione relativa alle osservazioni.

 

</dd> <dt>

*lpString* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa Unicode da analizzare.

</dd> <dt>

*cchString* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, della stringa Unicode indicata da *lpString*. L'applicazione imposta questo parametro su -1 se la stringa ha terminazione Null. Se l'applicazione imposta questo parametro su 0, la funzione recupera una stringa Unicode null (L" \\ 0") in *lpScripts* e restituisce 1.

</dd> <dt>

*lpScripts* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera una stringa con terminazione Null che rappresenta un elenco di script, usando la notazione a 4 caratteri usata in [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico. Ogni nome, incluso l'ultimo, è seguito da un punto e virgola.

In alternativa, questo parametro può **contenere NULL** se *cchScripts* è impostato su 0. In questo caso, la funzione restituisce le dimensioni richieste per il buffer di script.

</dd> <dt>

*cchScripts* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, per il buffer di script indicato da *lpScripts*.

In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione recupera **NULL** in *lpScripts* e restituisce le dimensioni richieste per il buffer di script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri recuperati nel buffer di output, incluso un carattere Null di terminazione, se ha esito positivo e *cchScripts* è impostato su un valore diverso da zero. La funzione restituisce 1 per indicare che non è stato trovato alcuno script, ad esempio quando la stringa di input contiene solo caratteri COMMON o INHERITED e GSS \_ ALLOW \_ INHERITED \_ COMMON non è impostato. Dato che ogni script trovato aggiunge cinque caratteri (quattro caratteri + delimitatore), una semplice operazione matematica fornisce il numero di script come (codice restituito \_ - 1) / 5.

Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che includono un carattere Null di terminazione, per il buffer dello script. Il numero di script è come descritto in precedenza.

La funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sugli errori, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BADDB. La funzione non è stata in grado di accedere ai dati. Questa situazione in genere non deve verificarsi e indica in genere un'installazione non erta, un problema del disco o simili.
-   ERRORE \_ BUFFER \_ INSUFFICIENTE. Le dimensioni del buffer specificate non erano sufficienti o non erano impostate in modo errato su **NULL.**
-   ERRORE \_ FLAG NON \_ VALIDI. I valori forniti per i flag non sono validi.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi di dominio [internazionalizzati (IDN).](handling-internationalized-domain-names--idns.md)

La determinazione dello script si basa sui valori di script pubblicati dal consorzio Unicode in , ad eccezione del fatto che i caratteri non assegnati hanno il valore <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> "Zzzz" (UNASSIGNED) anziché "Zyyy" (COMMON).

Ecco alcuni esempi del comportamento di questa funzione:



Stringa di input

*dwFlags*

*lpScripts*

Script

Microsoft.com

0

Latn;

Latino

Microsoft.com

GSS \_ CONSENTE \_ L'EREDITARIETÀ \_ COMUNE

Latn; Zyyy;

Latino + Comune

${ROWSPAN2}$Ni ño${REMOVE}$  

004E 0069 0241 006F

${ROWSPAN2}$GSS ALLOW \_ \_ INHERITED \_ COMMON${REMOVE}$  

${ROWSPAN2}$Latn;${REMOVE}$  

${ROWSPAN2}$Latin${REMOVE}$  

Usa LATIN SMALL LETTER N WITH TILDE

${ROWSPAN2}$Ni ño${REMOVE}$  

004E 0069 006E 0303 006F

${ROWSPAN2}$GSS ALLOW \_ \_ INHERITED \_ COMMON${REMOVE}$  

${ROWSPAN2}$Latn; Qaii;${REMOVE}$  

${ROWSPAN2}$Latin + Inherited${REMOVE}$  

Usa LA TILDE DI COMBINAZIONE

${ROWSPAN2}$Sp$Sp osof${REMOVE}$  

0053 0070 043e 043e 0066

${ROWSPAN2}$0${REMOVE}$  

${ROWSPAN2}$Latn; Cyrl;${REMOVE}$  

${ROWSPAN2}$Latin + Cirillico${REMOVE}$  

Usa LA LETTERA MINUSCOLA CIRILLICA O



U+f000

0

Zzzz;

Unassigned (Non assegnato)



U+f000

GSS \_ CONSENTE \_ L'EREDITARIETÀ \_ COMUNE

Zzzz;

Unassigned (Non assegnato)



 

Il file di intestazione e la DLL necessari fanno parte del download ["MICROSOFT Internationalized Domain Name (IDN) Mitigation APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) disponibile nell'Area [download MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                        |
| Componente ridistribuibile<br/>          | API di mitigazione IDN (Internationalized Domain Name) microsoft in Windows XP (SP2 o versione successiva), Windows Server 2003 (SP1 o versione successiva) o Windows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



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

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
