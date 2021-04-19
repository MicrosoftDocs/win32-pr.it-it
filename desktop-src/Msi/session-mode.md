---
description: Si tratta della proprietà Mode dell'oggetto Session. Questa proprietà è un valore che rappresenta il flag della modalità designata per la sessione di installazione corrente. La maggior parte dei flag della modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Proprietà Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333048"
---
# <a name="sessionmode-property"></a>Proprietà Session. Mode

Si tratta della proprietà **mode** dell'oggetto [**Session**](session-object.md) . Questa proprietà è un valore che rappresenta il flag della modalità designata per la sessione di installazione corrente. La maggior parte dei flag della modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.

La funzione [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) restituisce un valore booleano true o false, che indica se la proprietà specifica passata nella funzione è attualmente impostata (true) o non impostata (false).

Si noti che non tutti i valori della modalità di esecuzione del *flag* sono disponibili quando si chiama la proprietà **mode** da un'azione personalizzata posticipata. Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>Valore proprietà

Valore intero obbligatorio per il flag. I possibili valori sono i seguenti:



| Nome del flag                                                                                                                                                                                                                                                                                                | Significato                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**msiRunModeAdmin**</dt> <dt>0</dt> </dl>                                              | Installazione in modalità amministrativa, altrimenti installazione del prodotto.<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msiRunModeAdvertise**</dt> <dt>1</dt> </dl>                              | Annunciare la modalità di installazione.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msiRunModeMaintenance**</dt> <dt>2</dt> </dl>                      | Database in modalità manutenzione caricato.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt> </dl>      | Il rollback è abilitato.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msiRunModeLogEnabled**</dt> <dt>4</dt> </dl>                          | Il file di log è attivo.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msiRunModeOperations**</dt> <dt>5</dt> </dl>                          | Esecuzione o spooling delle operazioni.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt> </dl>                      | È necessario riavviare il computer (impostabile).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msiRunModeRebootNow**</dt> <dt>7</dt> </dl>                              | Per continuare l'installazione è necessario riavviare il computer (impostabile).<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msiRunModeCabinet**</dt> <dt>8</dt> </dl>                                      | Installazione di file da file CAB e file con la tabella media.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt> </dl>  | I file di origine utilizzano solo nomi di file brevi.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt> </dl> | I file di destinazione devono usare solo nomi di file brevi.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | Il sistema operativo è Windows 98/95.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msiRunModeZawEnabled**</dt> <dt>13</dt> </dl>                         | Il sistema operativo supporta la pubblicità di prodotti.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msiRunModeScheduled**</dt> <dt>16</dt> </dl>                             | [Azione personalizzata](custom-actions.md) posticipata chiamata dall'esecuzione dello script di installazione.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msiRunModeRollback**</dt> <dt>17</dt> </dl>                                 | [Azione personalizzata](custom-actions.md) posticipata chiamata dallo script di esecuzione del rollback.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msiRunModeCommit**</dt> <dt>18</dt> </dl>                                         | [Azione personalizzata](custom-actions.md) posticipata chiamata dallo script di esecuzione del commit.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



 

 




