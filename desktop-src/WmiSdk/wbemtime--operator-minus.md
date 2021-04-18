---
description: 'Operatore di sottrazione della classe WBEMTime (&\# 8211;) è stato sovraccaricato a:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Operatori WBEMTime:: operator-(WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318852"
---
# <a name="wbemtimeoperator--operators"></a>Operatori WBEMTime:: operator-

\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

L'operatore di sottrazione della classe [**WBEMTime**](wbemtime.md) () è stato sottomesso a overload per:

-   Sottrae un intervallo di tempo dal tempo di un oggetto per produrre un nuovo oggetto temporale che contiene il tempo risultante.
-   Sottrarre un'ora dal tempo dell'oggetto per produrre un nuovo oggetto intervallo di tempo che contiene la differenza tra le due volte.

### <a name="overload-list"></a>Elenco di overload



| Operatore                                                                         | Descrizione                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operatore-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Sottrae un **WBEMTime** da un **WBEMTime**.<br/>                         |
| [**operatore-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Sottrae un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) da un **WBEMTime**.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
