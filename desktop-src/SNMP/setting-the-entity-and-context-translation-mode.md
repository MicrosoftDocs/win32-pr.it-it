---
title: Impostazione della modalità di conversione dell'entità e del contesto
description: L'applicazione WinSNMP può specificare l'interpretazione e la traduzione dei parametri dell'entità e del contesto impostando la modalità di conversione dell'entità e del contesto. L'implementazione di Microsoft WinSNMP archivia la modalità in un database.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044417"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Impostazione della modalità di conversione dell'entità e del contesto

L'applicazione WinSNMP può specificare l'interpretazione e la traduzione dei parametri dell'entità e del contesto impostando la modalità di conversione dell'entità e del contesto. L'implementazione di Microsoft WinSNMP archivia la modalità in un database.

L'impostazione della modalità di conversione dell'entità e del contesto determina il modo in cui la funzione [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) e la funzione [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretano le stringhe di input. L'impostazione determina anche il tipo di stringa di output restituito dalle funzioni [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) . Per ulteriori informazioni, vedere [supporto per le stringhe di indirizzi IPX in WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).

L'implementazione restituisce l'entità predefinita corrente e la modalità di conversione del contesto nel parametro *nTranslateMode* della funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) . Per recuperare l'entità corrente e la modalità di conversione del contesto attiva per l'implementazione, un'applicazione può chiamare la funzione [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) in qualsiasi momento.

Seguono le modalità di conversione dell'entità e del contesto valide.

| Modalità                      | Significato                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ tradotta       | L'implementazione utilizza il database per tradurre i nomi descrittivi per le entità SNMP e gli oggetti gestiti. L'implementazione li converte nei componenti SNMPv1 o SNMPv2C.                                                                                                  |
| SNMPAPI non \_ tradotto \_ V1 | L'implementazione interpreta i parametri di entità SNMP come indirizzi di trasporto SNMP letterali e parametri di contesto come stringhe di comunità SNMP letterali. Per le entità di destinazione SNMPv2, l'implementazione crea messaggi SNMP in uscita contenenti un valore pari a zero nel campo versione. |
| SNMPAPI non \_ tradotto \_ v2 | L'implementazione interpreta i parametri dell'entità SNMP come indirizzi di trasporto SNMP e i parametri di contesto come stringhe di comunità SNMP letterali. Per le entità di destinazione SNMPv2, l'implementazione crea messaggi SNMP in uscita contenenti un valore pari a 1 nel campo versione.            |



 

L'implementazione tenta di associare le risorse nel database con l'indirizzo di trasporto letterale dell'entità di gestione.

Per modificare l'impostazione della modalità di conversione dell'entità e del contesto, è necessario che un'applicazione WinSNMP chiami la funzione [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) . Se la modalità di conversione richiesta non è valida, la funzione ha esito negativo e [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) restituisce la modalità snmpapi del codice di errore \_ \_ non valida.

 

 




