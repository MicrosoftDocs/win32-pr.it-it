---
description: Si tratta della proprietà Mode dell'oggetto Session. Questa proprietà è un valore che rappresenta il flag di modalità designato per la sessione di installazione corrente. La maggior parte dei flag di modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session.Mode - proprietà
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
ms.openlocfilehash: ed0c24280307cf368239ab88b5357924a3ee40d5a62444838e155aca2c0642f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629121"
---
# <a name="sessionmode-property"></a>Session.Mode - proprietà

Si tratta della **proprietà Mode** [**dell'oggetto**](session-object.md) Session. Questa proprietà è un valore che rappresenta il flag di modalità designato per la sessione di installazione corrente. La maggior parte dei flag di modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.

La [**funzione MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) restituisce un valore booleano TRUE o FALSE, che indica se la proprietà specifica passata alla funzione è attualmente impostata (TRUE) o non impostata (FALSE).

Si noti che non tutti i valori della modalità di esecuzione *del flag* sono disponibili quando si chiama la **proprietà Mode** da un'azione personalizzata posticipata. Per altre informazioni, vedere [Recupero di informazioni sul contesto per le azioni personalizzate di esecuzione posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md)

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
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msiRunModeAdvertise**</dt> <dt>1</dt> </dl>                              | Modalità di annuncio dell'installazione.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msiRunModeMaintenance**</dt> <dt>2</dt> </dl>                      | Database in modalità manutenzione caricato.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt> </dl>      | Il rollback è abilitato.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msiRunModeLogEnabled**</dt> <dt>4</dt> </dl>                          | Il file di log è attivo.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msiRunModeOperations**</dt> <dt>5</dt> </dl>                          | Esecuzione o spooling di operazioni.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt> </dl>                      | È necessario riavviare (impostabile).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msiRunModeRebootNow**</dt> <dt>7</dt> </dl>                              | Il riavvio è necessario per continuare l'installazione (impostabile).<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msiRunModeCabinet**</dt> <dt>8</dt> </dl>                                      | Installazione di file da file cab e file usando la tabella Media.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt> </dl>  | I file di origine usano solo nomi di file brevi.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt> </dl> | I file di destinazione usano solo nomi di file brevi.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | Il sistema operativo Windows 98/95.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msiRunModeZawEnabled**</dt> <dt>13</dt> </dl>                         | Il sistema operativo supporta la pubblicità dei prodotti.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msiRunModeScheduled**</dt> <dt>16</dt> </dl>                             | Azione personalizzata [posticipata chiamata](custom-actions.md) dall'esecuzione dello script di installazione.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msiRunModeRollback**</dt> <dt>17</dt> </dl>                                 | Azione personalizzata [posticipata chiamata](custom-actions.md) dallo script di esecuzione del rollback.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msiRunModeCommit**</dt> <dt>18</dt> </dl>                                         | Azione personalizzata [posticipata chiamata](custom-actions.md) dallo script di esecuzione del commit.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



 

 




