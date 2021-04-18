---
description: La funzione DeletePrinterDriverEx rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver. Questa funzione può anche eliminare versioni specifiche del driver.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Funzione DeletePrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313025"
---
# <a name="deleteprinterdriverex-function"></a>DeletePrinterDriverEx (funzione)

La funzione **DeletePrinterDriverEx** rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver. Questa funzione può anche eliminare versioni specifiche del driver.

## <a name="syntax"></a>Sintassi


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere eliminato il driver. Se questo parametro è **null**, la funzione eliminerà il driver della stampante dal computer locale.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere eliminato il driver, ad esempio Windows NT x86, Windows IA64 o Windows x64. Se questo parametro è **null**, il nome del driver viene eliminato dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*pDriverName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver da eliminare.

</dd> <dt>

*dwDeleteFlag* \[ in\]
</dt> <dd>

Opzioni per l'eliminazione di file e versioni del driver. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**\_ \_ versione specifica dell'eliminazione DPD \_**</dt> </dl> | Elimina la versione specificata in *dwVersionFlag*. Ciò non garantisce che il driver venga rimosso dall'elenco dei driver supportati per il server.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**\_Elimina \_ file inutilizzati DPD \_**</dt> </dl>             | Rimuove tutti i file di driver non utilizzati.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**DPD \_ Elimina \_ tutti \_ i file**</dt> </dl>                      | Elimina il driver solo se è possibile rimuovere tutti i file associati. L'operazione di eliminazione ha esito negativo se uno dei file del driver viene usato da un altro driver installato.<br/> |



 

Se \_ \_ \_ non viene specificata la versione specifica di DPD Delete, la funzione eliminerà tutte le versioni del driver se nessuna di esse è in uso. Se non \_ vengono eliminati \_ i file inutilizzati \_ o DPD \_ Delete \_ tutti \_ i file, la funzione non elimina i file del driver.

</dd> <dt>

*dwVersionFlag* \[ in\]
</dt> <dd>

Versione del driver da eliminare. Questo parametro può essere 0, 1, 2 o 3. Questo parametro viene usato solo se *dwDeleteFlag* include il \_ flag di \_ versione specifico dell'eliminazione DPD \_ .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Prima che la funzione elimini i file del driver, chiama la funzione **DrvDriverEvent** del driver, consentendo al driver di rimuovere tutti i file privati che non vengono usati. Per ulteriori informazioni su **DrvDriverEvent**, vedere Microsoft Windows Driver Development Kit (DDK).

Se i file dei driver sono attualmente caricati, la funzione li sposta in una directory Temp e li contrassegna per l'eliminazione al riavvio.

Prima di chiamare **DeletePrinterDriverEx**, è necessario eliminare tutti gli oggetti stampante che usano il driver della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterDriverExW** (Unicode) e **DeletePrinterDriverExA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 




