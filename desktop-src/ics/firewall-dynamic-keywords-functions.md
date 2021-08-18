---
title: Funzioni delle parole chiave dinamiche del firewall
description: Le parole chiave dinamiche del firewall contengono le funzioni seguenti.
keywords:
- Parole chiave dinamiche del firewall, funzioni
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: 1aacc30ecac9cddca5f986878da1ff633660152144e8ca2fe1440fdecfd61e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015651"
---
# <a name="firewall-dynamic-keywords-functions"></a>Funzioni delle parole chiave dinamiche del firewall

Le parole chiave dinamiche del firewall contengono le funzioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Richiede il recapito di notifiche relative alle modifiche a determinati oggetti di indirizzo di parola[chiave dinamica](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)( FW_DYNAMIC_KEYWORD_ADDRESS0 ). |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Annulla il recapito delle notifiche relative alle modifiche apportate a specifici oggetti di indirizzo di parola[chiave dinamica](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)( FW_DYNAMIC_KEYWORD_ADDRESS0 ). |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per aggiungere l'indirizzo della parola chiave dinamica specificato. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per eliminare l'indirizzo della parola chiave dinamica con l'ID specificato. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per enumerare gli indirizzi delle parole chiave dinamiche specifici in base all'ID. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per enumerare gli indirizzi delle parole chiave dinamiche in base al tipo. È possibile richiedere un subset specifico di oggetti in base ai flag di enumerazione passati. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per liberare gli struct di dati di indirizzo dinamico allocati dal servizio. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Tipo di puntatore a funzione del punto di ingresso nel servizio chiamato per aggiornare l'indirizzo della parola chiave dinamica con l'ID di input. |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento per le parole chiave dinamiche del firewall](firewall-dynamic-keywords-reference.md)
