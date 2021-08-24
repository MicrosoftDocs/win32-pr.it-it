---
description: SetDNSServerSearchOrder &\# 32; Il metodo della classe WMI usa una matrice di elementi stringa per impostare l'ordine di ricerca del server.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Metodo SetDNSServerSearchOrder della Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ae53996e2f8199d552909a186ab17e6b7ec89857c9be24dc4d8d4bfe583cfea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759801"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetDNSServerSearchOrder della classe NetworkAdapterConfiguration Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** usa una matrice di elementi stringa per impostare l'ordine di ricerca del server.

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DNSServerSearchOrder* \[ Pollici\]
</dt> <dd>

Elenco di indirizzi IP del server su cui eseguire query per i server DNS.

Esempio: 130.215.24.1 o 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) per un completamento corretto quando non è necessario alcun riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Completamento riuscito, riavvio non necessario** (0)
</dt> <dt>

**Completamento riuscito, riavvio necessario** (1)
</dt> <dt>

**Metodo non supportato in questa piattaforma** (64)
</dt> <dt>

**Errore sconosciuto** (65)
</dt> <dt>

**Non subnet mask** (66)
</dt> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)
</dt> <dt>

**Parametro di input non** valido (68)
</dt> <dt>

**Più di 5 gateway specificati** (69)
</dt> <dt>

**Indirizzo IP non valido** (70)
</dt> <dt>

**Indirizzo IP del gateway non valido** (71)
</dt> <dt>

**Si è verificato un errore durante l'accesso al Registro di sistema per le informazioni richieste** (72)
</dt> <dt>

**Nome di dominio non** valido (73)
</dt> <dt>

**Nome host non valido** (74)
</dt> <dt>

**Nessun server WINS primario/secondario definito** (75)
</dt> <dt>

**File non valido** (76)
</dt> <dt>

**Percorso di sistema non** valido (77)
</dt> <dt>

**Copia file non riuscita** (78)
</dt> <dt>

**Parametro di sicurezza non** valido (79)
</dt> <dt>

**Impossibile configurare il servizio TCP/IP** (80)
</dt> <dt>

**Impossibile configurare il servizio DHCP** (81)
</dt> <dt>

**Impossibile rinnovare il lease DHCP** (82)
</dt> <dt>

**Impossibile rilasciare il lease DHCP** (83)
</dt> <dt>

**IP non abilitato sulla scheda** (84)
</dt> <dt>

**IPX non abilitato sulla scheda** (85)
</dt> <dt>

**Errore dei limiti dei numeri di rete/frame** (86)
</dt> <dt>

**Tipo di frame non** valido (87)
</dt> <dt>

**Numero di rete non valido** (88)
</dt> <dt>

**Numero di rete duplicato** (89)
</dt> <dt>

**Parametro non in limiti** (90)
</dt> <dt>

**Accesso negato** (91)
</dt> <dt>

**Memoria insufficiente** (92)
</dt> <dt>

**Esiste già** (93)
</dt> <dt>

**Percorso, file o oggetto non trovato** (94)
</dt> <dt>

**Impossibile inviare una notifica al** servizio (95)
</dt> <dt>

**Impossibile inviare una notifica al servizio DNS** (96)
</dt> <dt>

**Interfaccia non configurabile** (97)
</dt> <dt>

**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)
</dt> <dt>

**DHCP non abilitato sulla scheda** (100)
</dt> <dt>

**Altro** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Si tratta di una chiamata al metodo dipendente dall'istanza che si applica in base all'adattatore. Dopo che i server DNS statici sono stati specificati per iniziare a usare Dynamic Host Configuration Protocol (DHCP) anziché i server DNS statici, è possibile chiamare il metodo senza fornire parametri "in".

## <a name="examples"></a>Esempio

[L'esempio VBScript Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) (Imposta l'ordine di ricerca dei server DNS per più computer in un'unità organizzativa) nella raccolta TechNet recupera o imposta l'ordine di ricerca del server DNS per più computer appartenenti a un'unità organizzativa.

[L'esempio modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript configura una scheda di rete associata a TCP/IP per l'uso di due server DNS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Attività WMI: Rete](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Attività WMI: Account e domini](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Supporto di IPv6 e IPv4 in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

