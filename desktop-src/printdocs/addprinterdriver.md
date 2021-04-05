---
description: La funzione AddPrinterDriver installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Funzione AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757859"
---
# <a name="addprinterdriver-function"></a>AddPrinterDriver (funzione)

La funzione **AddPrinterDriver** installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.

Per una maggiore flessibilità nell'installazione o nell'aggiornamento dei driver della stampante, utilizzare la funzione [**AddPrinterDriverEx**](addprinterdriverex.md) perché consente l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori di data e ora).

> [!Note]  
> Non è più consigliabile installare un driver della stampante senza un pacchetto driver. In alternativa, usare [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) .

 

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il driver.

Se *pname* è **null**, il driver verrà installato localmente.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pDriverInfo* .

Questo valore può essere 2, 3, 4, 6 o 8.

</dd> <dt>

*pDriverInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura contenente informazioni sul driver della stampante. Dipende dal valore di *Level*.



| Valore | Struttura unità stampante                  |
|-------|------------------------------------------|
| 2     | [**\_Informazioni driver \_ 2**](driver-info-2.md) |
| 3     | [**\_Informazioni driver \_ 3**](driver-info-3.md) |
| 4     | [**\_Informazioni driver \_ 4**](driver-info-4.md) |
| 6     | [**\_Informazioni driver \_ 6**](driver-info-6.md) |
| 8     | [**\_Informazioni driver \_ 8**](driver-info-8.md) |



 

Se il membro **pEnvironment** della struttura a cui punta *pDriverInfo* è **null**, viene usato l'ambiente corrente del chiamante/client (non di destinazione/Server).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Prima che un'applicazione chiami la funzione **AddPrinterDriver** , tutti i file richiesti dal driver devono essere copiati nella directory di driver della stampante del sistema. Un'applicazione può recuperare il nome di questa directory chiamando la funzione [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Un'applicazione può determinare quali driver della stampante sono attualmente installati chiamando la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterDriverW** (Unicode) e **AddPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**\_Informazioni driver \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informazioni driver \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informazioni driver \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informazioni driver \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

