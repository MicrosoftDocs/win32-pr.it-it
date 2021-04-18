---
description: In questa sezione vengono fornite le specifiche di riferimento per le costanti di manipolazione diretta.
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: Costanti di manipolazione diretta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5040191f22e92dcfb8c2ca26edd4080cd4cbb2be
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303944"
---
# <a name="direct-manipulation-constants"></a>Costanti di manipolazione diretta

In questa sezione vengono fornite le specifiche di riferimento per le costanti di [manipolazione diretta](direct-manipulation-portal.md) .

| Costante/valore                                                                                                                                                                                                                                                                         | Descrizione                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <dt>**DIRECTMANIPULATION \_**</dt> <dt>0xfffffffe</dt> KEYBOARDFOCUS </dl> | Specifica un ID puntatore pseudoclasse per emulare un contatto tocco tramite input da tastiera.<br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <dt>**DIRECTMANIPULATION \_**</dt> <dt>0xFFFFFFFD</dt> MOUSEFOCUS </dl>          | Specifica un ID puntatore pseudoclasse per emulare un contatto tocco tramite l'input del mouse.<br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <dt>**DIRECTMANIPULATION \_ \_Zoom minimo**</dt> <dt>0,1</dt> </dl>          | Specifica il limite di zoom minimo consentito pari al 10%.<br/>                               |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                              |
| IDL<br/>                      | <dl> <dt>DirectManipulation. idl</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Guida di riferimento alla manipolazione diretta](direct-manipulation-reference.md)
