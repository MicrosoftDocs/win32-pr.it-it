---
description: Il valore della proprietà Riepilogo oggetto indica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Proprietà Riepilogo oggetto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9d92328f142e4fd47567e92d4fe3bb7f016b0bf058b2932f7e1136687507e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627231"
---
# <a name="subject-summary-property"></a>Proprietà Riepilogo oggetto

Il valore della **proprietà Riepilogo** oggetto indica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.

È l'autore di un database di installazione, una trasformazione o un pacchetto patch a fornire il valore di questa proprietà nelle informazioni di riepilogo. Gli autori devono eseguire le operazioni seguenti per determinare il valore corretto.

-   Impostare la **proprietà Riepilogo** oggetto in un pacchetto di installazione sullo stesso valore della [**proprietà ProductName.**](productname.md)
-   Impostare la **proprietà Riepilogo** oggetto in una trasformazione sullo stesso valore della proprietà **Riepilogo** oggetto nel pacchetto di installazione originale.
-   Impostare la **proprietà Riepilogo** oggetto nelle informazioni di riepilogo di un pacchetto patch su una breve descrizione della patch che include il nome del prodotto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




