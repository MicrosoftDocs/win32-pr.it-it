---
description: Aggiunge un nome di rete locale alternativo per il computer da cui viene chiamato.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Funzione AddLocalAlternateComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 90945188209abdcaf16a7250e43db2af9a99ab4a3fbb55b8baabf0ea610c99e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668683"
---
# <a name="addlocalalternatecomputername-function"></a>Funzione AddLocalAlternateComputerName

Aggiunge un nome di rete locale alternativo per il computer da cui viene chiamato.

## <a name="syntax"></a>Sintassi


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpDnsFQHostname* \[ Pollici\]
</dt> <dd>

Nome alternativo da aggiungere. Il nome deve essere nel formato **ComputerNameDnsFullyQualified** come definito nell'enumerazione [**COMPUTER NAME \_ \_ FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) e la funzione [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) deve essere in grado di convalidarlo con il relativo formato impostato su **DnsNameHostnameFull**.

</dd> <dt>

*flag ulFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **ERROR \_ SUCCESS**. Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero. Tra i codici di errore restituiti ci sono i seguenti:



| Codice restituito                                                                                               | Descrizione                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>  | Indica che il *parametro lpDnsFQHostname* non punta a un nome DNS valido o che il parametro *ulFlags* non è uguale a zero.<br/> |
| <dl> <dt>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**</dt> </dl> | Memoria insufficiente per completare l'operazione.<br/>                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Libreria<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Nomi Unicode e ANSI<br/> | **AddLocalAlternateComputerNameW** (Unicode) e **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FORMATO \_ NOME \_ COMPUTER**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
