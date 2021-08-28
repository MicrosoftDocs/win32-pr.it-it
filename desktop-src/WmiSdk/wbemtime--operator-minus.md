---
description: 'Operatore di sottrazione della classe WBEMTime (&\# 8211;) è stato sottoposto a overload per:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: Operatori WBEMTime::operator- (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7748020c1dcf1e332384c3a29c18b37da53e020f42d6cb608d9bf3233608aaaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120751"
---
# <a name="wbemtimeoperator--operators"></a>Operatori WBEMTime::operator-

\[La [**classe WBEMTime**](wbemtime.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

L'operatore di sottrazione della classe [**WBEMTime**](wbemtime.md) ( ) è stato sottoposto a overload in:

-   Sottrarre un intervallo di tempo dal tempo di un oggetto per produrre un nuovo oggetto time che contiene l'ora risultante.
-   Sottrarre un tempo dal tempo dell'oggetto per produrre un nuovo oggetto intervallo di tempo che contiene la differenza tra le due volte.

### <a name="overload-list"></a>Elenco di overload



| Operatore                                                                         | Descrizione                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operator-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Sottrae **un WBEMTime** da **un oggetto WBEMTime.**<br/>                         |
| [**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | [**Sottrae un oggetto WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) da un oggetto **WBEMTime.**<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
