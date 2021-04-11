---
description: Il metodo SelectFile costruisce un comando APDU (Application Protocol Data Unit) che imposta un file elementare corrente all'interno di un canale logico. I comandi successivi possono fare riferimento in modo implicito al file corrente tramite il canale logico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'Metodo ISCardISO7816:: SelectFile (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231715"
---
# <a name="iscardiso7816selectfile-method"></a>Metodo ISCardISO7816:: SelectFile

\[Il metodo **SelectFile** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **SelectFile** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che imposta un file elementare corrente all'interno di un canale logico. I comandi successivi possono fare riferimento in modo implicito al file corrente tramite il canale logico.

La selezione di una directory (DF) nell'archivio file delle schede, che può essere la radice (MF) del file Store, lo rende il valore DF corrente. Dopo questa selezione, è possibile fare riferimento a un file elementare corrente implicito tramite il canale logico.

Selezionando un file elementare, il file selezionato e il relativo padre vengono impostati come file correnti.

Dopo la reimpostazione della risposta, MF viene selezionato in modo implicito tramite il canale logico di base, a meno che non venga specificato diversamente nei byte cronologici o nella stringa di dati iniziale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Controllo di selezione.



| P1 (byte superiore in Word): 8 7 6 5 4 3 2 1                                                                                                                                                            | Significato                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000XX**</dt><dt></dt> </dl> | Seleziona ID file<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF o MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | DF figlio<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF in DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | DF padre del DF corrente<br/> |



 

Quando P1 = 00, la scheda è nota a causa di una specifica codifica dell'ID file o a causa del contesto di esecuzione del comando se il file da selezionare è MF, DF o EF.

Quando P1-P2 = 0000, se viene fornito un ID file, deve essere univoco negli ambienti seguenti:

-   Elementi figlio immediati del DF corrente
-   DF padre
-   Elementi figlio immediati del DF padre

Se P1-P2 = 0000 e il campo dati è vuoto o uguale a 3F00, selezionare MF.

Quando P1 = 04, il campo dati è un nome DF, probabilmente troncato a destra.

Se supportato, i comandi successivi con lo stesso campo dati dovranno selezionare DFs i cui nomi corrispondono a quelli del campo dati, ovvero iniziano con il campo dati del comando. Se la scheda accetta il comando con un campo dati vuoto, è possibile selezionare in successione tutti o un subset del DFs.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Controllo di selezione.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Dati per l'operazione, se necessario; altrimenti, **null**. I tipi di dati passati in questo parametro includono:

-   ID file
-   percorso da MF
-   percorso dal DF corrente
-   Nome DF

</dd> <dt>

*lBytesToRead* \[ in\]
</dt> <dd>

Vuoto (ovvero 0) o lunghezza massima dei dati previsti nella risposta.

</dd> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.

Al ritorno, viene compilato con il comando APDU creato da questa operazione. Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Se non diversamente specificato, l'esecuzione corretta del comando incapsulato modifica lo stato di sicurezza in base alle regole seguenti:

-   Quando il file elementare corrente viene modificato o quando non è presente alcun file elementare corrente, lo stato di sicurezza specifico di un precedente file elementare corrente viene perso.
-   Quando la directory FileStore corrente (DF) è discendente di o identica alla precedente DF corrente, lo stato di sicurezza specifico del DF corrente viene perso. Viene mantenuto lo stato di sicurezza comune a tutti i predecessori comuni del nuovo DF corrente.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
