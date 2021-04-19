---
description: La funzione AddPrinterDriverEx installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Funzione AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311565"
---
# <a name="addprinterdriverex-function"></a>AddPrinterDriverEx (funzione)

La funzione **AddPrinterDriverEx** installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver. Oltre a disporre delle funzionalità di [**AddPrinterDriver**](addprinterdriver.md), dispone anche di opzioni che consentono l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori temporali dei file).

> [!Note]  
> Non è più consigliabile installare un driver della stampante senza un pacchetto driver. In alternativa, usare [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) .

 

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il driver. Se questo parametro è **null**, la funzione installa il driver nel computer locale.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pDriverInfo* . Questo valore può essere 2, 3, 4, 6 o 8.

</dd> <dt>

*pDriverInfo* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura contenente informazioni sul driver della stampante. Può essere uno dei seguenti.



| Valore del livello                                                                                       | \_Struttura informazioni \_ \* driver                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**\_Informazioni driver \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**\_Informazioni driver \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**\_Informazioni driver \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**\_Informazioni driver \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**\_Informazioni driver \_ 8**](driver-info-8.md)<br/> |



 

Se il membro **pEnvironment** della struttura a cui punta *pDriverInfo* è **null**, la funzione usa l'ambiente corrente del chiamante/client, non l'ambiente del server di destinazione.

</dd> <dt>

*dwFileCopyFlags* \[ in\]
</dt> <dd>

Opzioni per la copia dei file del driver. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ Copia \_ tutti \_ i file**</dt> </dl>                | Aggiungere il driver della stampante e copiare tutti i file nella Directory Printer-driver. I timestamp del file vengono ignorati con questa opzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ Copia \_ dalla \_ Directory**</dt> </dl> | Aggiungere il driver della stampante utilizzando i nomi di file completi specificati nella [**struttura \_ informazioni driver \_ 6**](driver-info-6.md) . Questo flag è ORed insieme a uno degli altri flag di copia. Se questo flag è impostato, **AddPrinterDriverEx** avrà esito negativo se i file non esistono dove sono specificati nella struttura di **informazioni del \_ driver \_ 6** . Non è necessario copiare i file nella directory del driver della stampante del sistema. Vedere la sezione Osservazioni.<br/> **Windows 2000:** Questo flag non è supportato.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ Copia \_ nuovi \_ file**</dt> </dl>                | Aggiungere il driver della stampante e copiare i file nella directory del driver della stampante più recenti rispetto a tutti i file corrispondenti attualmente in uso. Questo flag emula il comportamento di [**AddPrinterDriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**\_downgrade Strict di APD \_**</dt> </dl>           | Aggiungere il driver della stampante solo se tutti i file nella directory del driver della stampante sono più vecchi di tutti i file corrispondenti attualmente in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**aggiornamento di APD \_ strict \_**</dt> </dl>                 | Aggiungere il driver della stampante solo se tutti i file nella directory del driver della stampante sono più recenti rispetto ai file attualmente in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Se il driver della stampante presenta problemi di utilizzo del sistema operativo, **AddPrinterDriverEx** avrà esito negativo con uno dei codici di errore seguenti:



| Codice di errore                      | Significato                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_driver della stampante di errore \_ \_ bloccato | Il driver non funziona nel sistema operativo.                                                                                                         |
| \_ \_ avviso driver stampante \_ errore  | Il driver non è affidabile sul sistema operativo. Tuttavia, se \_ \_ \_ si specifica il driver APD install warningd, il driver viene installato e non viene fornito alcun avviso. |



 

Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Prima di chiamare la funzione **AddPrinterDriverEx** , tutti i file richiesti dal driver devono essere copiati nella directory di driver della stampante del sistema. Per recuperare il nome di questa directory, chiamare la funzione [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Per determinare i driver della stampante attualmente installati, chiamare la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Se il driver della stampante è stato aggiunto correttamente, la funzione chiama la funzione DrvDriverEvent (DRIVER \_ Event \_ Initialize, Level, driver \_ info \_ \* , lParam) per consentire al driver di eseguire le inizializzazioni richieste durante l'installazione di un driver della stampante. Per ulteriori informazioni su **DrvDriverEvent**, vedere Microsoft Windows Driver Development Kit (DDK)

Il driver non deve usare una chiamata dell'interfaccia utente durante la chiamata a **DrvDriverEvent**. Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce VendorSetup nel file con estensione inf della stampante o, per Plug and Play dispositivi, il programma di installazione può usare un programma di coinstallazione specifico del dispositivo. Per ulteriori informazioni su VendorSetup, vedere DDK.

I file a cui viene fatto riferimento nella struttura di [**informazioni sul driver \_ \_ 6**](driver-info-6.md) devono essere locali rispetto al computer da cui viene effettuata la chiamata. Un nome file può essere un nome UNC purché il nome UNC sia il computer locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterDriverExW** (Unicode) e **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**\_Informazioni driver \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informazioni driver \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informazioni driver \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informazioni driver \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

