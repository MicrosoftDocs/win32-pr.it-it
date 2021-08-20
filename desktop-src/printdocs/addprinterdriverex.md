---
description: La funzione AddPrinterDriverEx installa un driver della stampante locale o remoto e collega i file di configurazione, dati e driver.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Funzione AddPrinterDriverEx (Winspool.h)
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
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868810"
---
# <a name="addprinterdriverex-function"></a>Funzione AddPrinterDriverEx

La **funzione AddPrinterDriverEx** installa un driver della stampante locale o remoto e collega i file di configurazione, dati e driver. Oltre a disporre delle funzionalità di [**AddPrinterDriver,**](addprinterdriver.md)include anche opzioni che consentono l'aggiornamento rigoroso, il downgrade rigoroso, la copia solo dei file più nuovi e la copia di tutti i file (indipendentemente dal timestamp dei file).

> [!Note]  
> Non è più consigliabile installare un driver della stampante senza un pacchetto driver. In [**alternativa, usare InstallPrinterDriverFromPackage.**](installprinterdriverfrompackage.md)

 

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

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui deve essere installato il driver. Se questo parametro è **NULL,** la funzione installa il driver nel computer locale.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Versione della struttura a cui *punta pDriverInfo.* Questo valore può essere 2, 3, 4, 6 o 8.

</dd> <dt>

*pDriverInfo* \[ in, out\]
</dt> <dd>

Puntatore a una struttura contenente informazioni sul driver della stampante. Può essere uno dei seguenti.



| Valore del livello                                                                                       | Struttura \_ DRIVER INFO \_ \*                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**DRIVER \_ INFO \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMAZIONI \_ DRIVER \_ 8**](driver-info-8.md)<br/> |



 

Se il **membro pEnvironment** della struttura a cui punta *pDriverInfo* è **NULL,** la funzione usa l'ambiente corrente del chiamante/client, non l'ambiente del server/destinazione.

</dd> <dt>

*dwFileCopyFlags* \[ Pollici\]
</dt> <dd>

Opzioni per la copia dei file del driver. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ COPY \_ ALL \_ FILES**</dt> </dl>                | Aggiungere il driver della stampante e copiare tutti i file nella directory printer-driver. I timestamp dei file vengono ignorati con questa opzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ COPY \_ FROM \_ DIRECTORY**</dt> </dl> | Aggiungere il driver della stampante usando i nomi di file completi specificati nella [**struttura DRIVER \_ INFO \_ 6.**](driver-info-6.md) Questo flag è ORed insieme a uno degli altri flag di copia. Se questo flag è impostato, **AddPrinterDriverEx** avrà esito negativo se i file non esistono dove sono specificati per esistere dalla **struttura DRIVER INFO \_ \_ 6.** Non è necessario copiare i file nella directory printer-driver del sistema. Vedere la sezione Osservazioni.<br/> **Windows 2000:** Questo flag non è supportato.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ COPY \_ NEW \_ FILES**</dt> </dl>                | Aggiungere il driver della stampante e copiare i file nella directory printer-driver più recente rispetto ai file corrispondenti attualmente in uso. Questo flag emula il comportamento di [**AddPrinterDriver.**](addprinterdriver.md)<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**APD \_ STRICT \_ DOWNGRADE**</dt> </dl>           | Aggiungere il driver della stampante solo se tutti i file nella directory printer-driver sono meno recenti rispetto ai file corrispondenti attualmente in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**APD \_ STRICT \_ UPGRADE**</dt> </dl>                 | Aggiungere il driver della stampante solo se tutti i file nella directory printer-driver sono più nuovi rispetto ai file corrispondenti attualmente in uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Se è noto che il driver della stampante ha problemi con il sistema operativo, **AddPrinterDriverEx** avrà esito negativo con uno dei codici di errore seguenti:



| Codice di errore                      | Significato                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ DEL DRIVER DELLA STAMPANTE \_ \_ BLOCCATO | Il driver non funziona nel sistema operativo.                                                                                                         |
| ERRORE \_ DEL DRIVER DELLA STAMPANTE \_ \_ AVVISATO  | Il driver non è affidabile nel sistema operativo. Tuttavia, se il \_ driver APD INSTALL WARNED è \_ \_ specificato, il driver viene installato e non viene visualizzato alcun avviso. |



 

Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante deve avere [seLoadDriverPrivilege.](/windows/desktop/SecAuthZ/authorization-constants)

Prima di chiamare **la funzione AddPrinterDriverEx,** tutti i file richiesti dal driver devono essere copiati nella directory printer-driver del sistema. Per recuperare il nome di questa directory, chiamare la [**funzione GetPrinterDriverDirectory.**](getprinterdriverdirectory.md)

Per determinare quali driver della stampante sono attualmente installati, chiamare [**la funzione EnumPrinterDrivers.**](enumprinterdrivers.md)

Se il driver della stampante è stato aggiunto correttamente, la funzione chiama la funzione DrvDriverEvent (DRIVER \_ EVENT \_ INITIALIZE, Level, DRIVER \_ INFO , lparam ) per consentire al driver di eseguire le inizializzazioni necessarie durante l'installazione di un driver della \_ \* stampante. Per altre informazioni su **DrvDriverEvent,** vedere Microsoft Windows Driver Development Kit (DDK)

Il driver non deve usare una chiamata all'interfaccia utente durante la chiamata **a DrvDriverEvent.** Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce VendorSetup nel file inf della stampante oppure, per i dispositivi Plug and Play, il programma di installazione può usare un co-programma di installazione specifico del dispositivo. Per altre informazioni su VendorSetup, vedere DDK.

I file a cui viene fatto riferimento [**nella struttura DRIVER INFO \_ \_ 6**](driver-info-6.md) devono essere locali rispetto al computer da cui viene effettuata la chiamata. Un nome file può essere un nome UNC, purché il nome UNC sia il computer locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterDriverExW** (Unicode) e **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**DRIVER \_ INFO \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL DRIVER \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriverdirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

