---
description: Nella tabella seguente sono elencati i metodi CHString.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: Classe CHString (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 4da0ee10493931c46da0879caf39ce5a1ac186cbb11dc4379343ea21120fac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109189"
---
# <a name="chstring-class"></a>Classe CHString

\[La **classe CHString** fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Nella tabella seguente sono elencati **i metodi CHString.**

## <a name="members"></a>Membri

La **classe CHString** ha questi tipi di membri:

-   [Costruttori](#constructors)
-   [Metodi](#methods)
-   [Operatori](#operators)

### <a name="constructors"></a>Costruttori

La **classe CHString** ha questi costruttori.



| Costruttore                           | Descrizione                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Costruisce **stringhe CHString** in vari modi.<br/> |



 

### <a name="methods"></a>Metodi

La **classe CHString** include questi metodi.



| Metodo                                                    | Descrizione                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Alloca un BSTR dai **dati CHString.**<br/>                                                            |
| [**Collate**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Confronta due stringhe (con distinzione tra maiuscole e minuscole; usa informazioni specifiche delle impostazioni locali).<br/>                            |
| [**Confronto**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Confronta due stringhe (con distinzione tra maiuscole e minuscole).<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Confronta due stringhe (senza distinzione tra maiuscole e minuscole).<br/>                                                            |
| [**Empty**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Forza la lunghezza di una stringa pari a 0 (zero).<br/>                                                            |
| [**Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Di overload. Trova un carattere o una sottostringa all'interno di una stringa più grande.<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Trova il primo carattere corrispondente da un set.<br/>                                                      |
| [**Formato**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Di overload. Formatta la stringa come **sprintf.**<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Di overload. Formatta una stringa di messaggio.<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Formatta la stringa come **vsprintf.**<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Rimuove l'overhead di questa stringa liberando la memoria aggiuntiva allocata in precedenza alla stringa.<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Restituisce le dimensioni del buffer di stringhe.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Di overload. Restituisce il carattere in una posizione specificata.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Restituisce un puntatore ai caratteri nella **stringa CHString.**<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Restituisce un puntatore ai caratteri nella stringa **CHString,** troncando alla lunghezza specificata.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Restituisce un puntatore ai dati nella **stringa CHString.**<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Restituisce il numero di caratteri Unicode in una **stringa CHString.**<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Verifica se una **stringa CHString** non contiene caratteri.<br/>                                         |
| [**Sinistra**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Estrae la parte sinistra di una stringa,ad esempio la funzione **LEFT$ di** base.<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Carica una stringa **CHString** esistente da un file di risorse.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Disabilita il conteggio dei riferimenti e protegge la stringa nel buffer.<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Converte tutti i caratteri in questa stringa in caratteri minuscoli.<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Inverte i caratteri in questa stringa.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Converte tutti i caratteri in questa stringa in caratteri maiuscoli.<br/>                              |
| [**Metà**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Di overload. Estrae la parte intermedia di una stringa ,ad esempio la funzione **MID$ di** base.<br/>                |
| [**Releasebuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Rilascia il controllo del buffer restituito da [**GetBuffer.**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Trova un carattere all'interno di una stringa più grande. inizia dalla fine.<br/>                                      |
| [**va bene**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Estrae la parte destra di una stringa ,ad esempio la funzione **RIGHT$ di** base.<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Imposta un carattere in una determinata posizione.<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Estrae una sottostringa che contiene solo i caratteri non presenti nel set.<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Estrae una sottostringa che contiene solo i caratteri in un set.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Taglia gli spazi vuoti iniziali dalla stringa.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Taglia gli spazi vuoti finali dalla stringa.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Abilita il conteggio dei riferimenti e rilascia la stringa nel buffer.<br/>                                   |



 

### <a name="operators"></a>Operatori
`
The **CHString** class has these operators.`



| Operatore                                                                                            | Descrizione                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**operatore != (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Confronta due **oggetti CHString per verifica** della disuguaglianza.<br/>                                                             |
| [**operatore != (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Confronta un **oggetto CHString con** un **LPCWSTR** per verifica della disuguaglianza.<br/>                                             |
| [**Operatore \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Restituisce il carattere in corrispondenza della sostituzione dell'operatore di posizione specificata [**per GetAt.**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))<br/> |
| [**operatore +**](chstring--operator-plus.md)                                                       | Concatena due stringhe e restituisce una nuova stringa.<br/>                                                     |
| [**operatore +=**](chstring--operator-plus-equal.md)                                                | Concatena una nuova stringa alla fine di una stringa esistente.<br/>                                            |
| [**operator < (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Confronta un **oggetto CHString** con un **oggetto LPCWSTR.**<br/>                                                            |
| [**operator < (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Confronta due **oggetti CHString.**<br/>                                                                            |
| [**operator <= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Confronta due **oggetti CHString.**<br/>                                                                            |
| [**operator <= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Confronta un **oggetto CHString** con un **oggetto LPCWSTR.**<br/>                                                            |
| [**operator =**](chstring--operator-equal.md)                                                      | Assegna un nuovo valore a una **stringa CHString.**<br/>                                                          |
| [**operatore == (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Confronta due **oggetti CHString per** verificane l'uguaglianza.<br/>                                                               |
| [**operatore == (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Confronta un **oggetto CHString con** un **LPCWSTR per** verificane l'uguaglianza.<br/>                                               |
| [**operator > (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Confronta due **oggetti CHString.**<br/>                                                                            |
| [**operator > (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Confronta un **oggetto CHString** con un **oggetto LPCWSTR.**<br/>                                                            |
| [**operator >= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Confronta due **oggetti CHString.**<br/>                                                                            |
| [**operator >= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Confronta un **oggetto CHString** con un **oggetto LPCWSTR.**<br/>                                                            |
| [**operatore LPCWSTR**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Accede direttamente ai caratteri archiviati in **una stringa CHString** come stringa di tipo C.<br/>                      |



 

## <a name="remarks"></a>Commenti

Il distruttore per la classe è **CHString::~CHString.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChString.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



