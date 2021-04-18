---
description: Dopo l'assegnazione degli indirizzi, TAPI assegna gli identificatori di indirizzo agli indirizzi.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificatori di indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306332"
---
# <a name="address-identifiers"></a>Identificatori di indirizzo

Dopo l'assegnazione degli indirizzi, TAPI assegna gli identificatori di indirizzo agli indirizzi. Un *identificatore di indirizzo* è un numero compreso tra 0 e il numero di indirizzi sulla riga meno uno. Un identificatore di indirizzo è un numero permanente assegnato a un determinato dispositivo e rimane costante anche negli aggiornamenti del sistema operativo. La combinazione di [identificatore di dispositivo](device-identifier-ovr.md) e identificatore di indirizzo identifica in modo univoco un determinato indirizzo.

**TAPI 2. x:** Le applicazioni ottengono un identificatore di indirizzo (e un identificatore del dispositivo) durante una chiamata a [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), nella struttura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) o in una chiamata a [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**TAPI 3. x:** [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) denominato *AddressCap* impostato sul membro **AC \_ ADDRESSID** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) restituirà il parametro *plCapability* impostato sull'ID indirizzo corrente.

 

 
