---
title: Impostazione della modalità di conversione di entità e contesto
description: L'applicazione WinSNMP può specificare l'interpretazione e la traduzione dei parametri di entità e contesto impostando la modalità di conversione dell'entità e del contesto. L'implementazione Microsoft WinSNMP archivia la modalità in un database.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab459c0b33ffe1cc43c81858b57ec55942f61f2b5b736ca0124f31f52cc960d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009059"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Impostazione della modalità di conversione di entità e contesto

L'applicazione WinSNMP può specificare l'interpretazione e la traduzione dei parametri di entità e contesto impostando la modalità di conversione dell'entità e del contesto. L'implementazione Microsoft WinSNMP archivia la modalità in un database.

L'impostazione della modalità di conversione dell'entità e del contesto determina il modo in cui la [**funzione SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) e la funzione [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretano le stringhe di input. L'impostazione determina anche il tipo di stringa di output restituito dalla [**funzione SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) [**e SnmpContextToStr.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) Per altre informazioni, vedere [Supporto per le stringhe di indirizzi IPX in WinSNMP.](support-for-ipx-address-strings-in-winsnmp.md)

L'implementazione restituisce l'entità predefinita corrente e la modalità di conversione del contesto nel *parametro nTranslateMode* della [**funzione SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) Per recuperare l'entità corrente e la modalità di conversione del contesto in vigore per l'implementazione, un'applicazione può chiamare la [**funzione SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) in qualsiasi momento.

Seguono le modalità di conversione di entità e contesto valide.

| Mode                      | Significato                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ CONVERTITO       | L'implementazione usa il database per convertire i nomi descrittivi per le entità SNMP e gli oggetti gestiti. L'implementazione li converte nei relativi componenti SNMPv1 o SNMPv2C.                                                                                                  |
| SNMPAPI \_ UNTRANSLATED \_ V1 | L'implementazione interpreta i parametri di entità SNMP come indirizzi di trasporto SNMP letterali e i parametri di contesto come stringhe letterali della community SNMP. Per le entità di destinazione SNMPv2, l'implementazione crea messaggi SNMP in uscita che contengono un valore pari a zero nel campo della versione. |
| SNMPAPI \_ UNTRANSLATED \_ V2 | L'implementazione interpreta i parametri di entità SNMP come indirizzi di trasporto SNMP e i parametri di contesto come stringhe letterali della community SNMP. Per le entità di destinazione SNMPv2, l'implementazione crea messaggi SNMP in uscita che contengono il valore 1 nel campo della versione.            |



 

L'implementazione tenta di associare le risorse nel proprio database all'indirizzo di trasporto letterale dell'entità di gestione.

Per modificare l'impostazione della modalità di conversione di entità e contesto, un'applicazione WinSNMP deve chiamare [**la funzione SnmpSetTranslateMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) Se la modalità di conversione richiesta non è valida, la funzione ha esito negativo e [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) restituisce il codice di errore SNMPAPI \_ MODE \_ INVALID.

 

 




