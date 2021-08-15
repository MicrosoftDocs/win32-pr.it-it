---
description: Modifica la modalità di avvio di un servizio \_ SystemDriver Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Metodo ChangeStartMode della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e2067ae7da8a6f112671237ebc7f77dd26644c5e0b2fa0b77a443c160468581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959130"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Metodo ChangeStartMode della classe SystemDriver Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un [**servizio \_ SystemDriver Win32.**](win32-systemdriver.md)

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartMode* \[ Pollici\]
</dt> <dd>

Modalità di avvio del Windows di base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio ("Avvio")**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("Sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("Automatico")


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("Disabilitato")


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il servizio è stato modificato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Servizi dipendenti in esecuzione** (3)
</dt> <dt>

**Controllo del servizio non** valido (4)
</dt> <dt>

**Il servizio non può accettare il controllo** (5)
</dt> <dt>

**Servizio non attivo** (6)
</dt> <dt>

**Timeout richiesta di servizio** (7)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Servizio già in esecuzione** (10)
</dt> <dt>

**Database del servizio bloccato** (11)
</dt> <dt>

**Dipendenza del servizio eliminata** (12)
</dt> <dt>

**Errore di dipendenza del servizio** (13)
</dt> <dt>

**Servizio disabilitato** (14)
</dt> <dt>

**Accesso al servizio non riuscito** (15)
</dt> <dt>

**Servizio contrassegnato per l'eliminazione** (16)
</dt> <dt>

**Thread senza servizio** (17)
</dt> <dt>

**Dipendenza circolare dello stato** (18)
</dt> <dt>

**Nome duplicato stato** (19)
</dt> <dt>

**Stato Nome non valido** (20)
</dt> <dt>

**Parametro stato non valido** (21)
</dt> <dt>

**Stato Account del servizio non valido** (22)
</dt> <dt>

**Il servizio di stato esiste** (23)
</dt> <dt>

**Servizio già sospeso** (24)
</dt> <dt>

**Altro** (25 4294967295)
</dt> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

