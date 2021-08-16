---
description: Windows Dispositivi portatili supporta le proprietà degli appuntamenti seguenti.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Proprietà Appointment (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2ba82c12dfffb0367ab61d355d6e256ab5d97bfbeef3e4a588f3a76a5651f9b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843591"
---
# <a name="appointment-properties"></a>Proprietà appuntamento

Windows Dispositivi portatili supporta le proprietà degli appuntamenti seguenti.



| Proprietà                                   | VarType        | Descrizione                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **PARTECIPANTI \_ ACCETTATI PER \_ APPUNTAMENTI WPD \_**  | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola dei partecipanti che hanno accettato l'appuntamento.             |
| **PARTECIPANTI RIFIUTATI PER UN APPUNTAMENTO WPD \_ \_ \_**  | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola dei partecipanti che hanno rifiutato l'appuntamento.             |
| **POSIZIONE DEGLI APPUNTAMENTI WPD \_ \_**             | VT \_ LPWSTR     | Posizione dell'appuntamento descrittiva per il lettore, ad esempio "Building 5, Room 7".    |
| **PARTECIPANTI \_ FACOLTATIVI DI \_ APPUNTAMENTI WPD \_**  | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola dei partecipanti facoltativi per l'appuntamento.                  |
| **PARTECIPANTI OBBLIGATORI \_ DELL'APPUNTAMENTO WPD \_ \_**  | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola dei partecipanti necessari per l'appuntamento.                  |
| **RISORSE PER APPUNTAMENTI WPD \_ \_**            | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola delle risorse necessarie per l'appuntamento.                  |
| **PARTECIPANTI PROVVISORI DI APPUNTAMENTI WPD \_ \_ \_** | **VT \_ LPWSTR** | Elenco delimitato da punto e virgola dei partecipanti che hanno accettato provvisoriamente l'appuntamento. |
| **TIPO DI APPUNTAMENTO WPD \_ \_**                 | **VT \_ LPWSTR** | Tipo di appuntamento, ad esempio"Personale", "Azienda" e così via.              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




