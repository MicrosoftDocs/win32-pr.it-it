---
description: Rappresenta una coppia chiave/valore.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318342"
---
# <a name="msvm_kvpexchangedataitem-class"></a>\_Classe MSVM KvpExchangeDataItem

Rappresenta una coppia chiave/valore.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>Members

La **classe \_ KvpExchangeDataItem di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ KvpExchangeDataItem di MSVM** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte relativa al valore della coppia chiave/valore.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte chiave della coppia chiave/valore.



| Chiave                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>CSDVersion</dt> </dl>                 | Stringa che rappresenta la Service Pack più recente installata nel sistema guest. Ad esempio, "Service Pack 2". Se non è stato installato alcun Service Pack, questa stringa è vuota.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | Stringa che rappresenta il nome DNS completo che identifica in modo univoco il computer locale. Questo nome è una combinazione del nome host DNS e del nome di dominio DNS, usando il formato *hostname*. *NomeDominio*. Se il computer locale è un nodo di un cluster, questo valore è il nome DNS completo del server virtuale del cluster. Questo valore corrisponde al nome restituito dalla funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) quando il parametro *NameType* è "ComputerNameDnsFullyQualified".<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | Stringa che rappresenta la versione del Integration Services attualmente installata nella macchina virtuale Guest (ad esempio, "6.1.7000.0").<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv4 attualmente assegnati alla macchina virtuale guest. L'elenco viene aggiornato automaticamente ogni volta che viene apportata una modifica alla configurazione TCP/IP nella macchina virtuale guest. Ogni indirizzo è rappresentato nella notazione decimale del punto. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv6 attualmente assegnati alla macchina virtuale guest. L'elenco viene aggiornato automaticamente ogni volta che viene apportata una modifica alla configurazione TCP/IP nella macchina virtuale guest. Ogni indirizzo è rappresentato nella notazione esadecimale con due punti. Gli elenchi IPv4 e IPv6 non sono sempre sincronizzati.<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | Stringa che rappresenta il numero di build del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | Stringa che rappresenta l'edizione (SKU) del sistema operativo della macchina virtuale guest. Per un elenco di valori possibili, vedere la funzione [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | Stringa che rappresenta il nome del sistema operativo. Questo valore deriva dalla voce del registro di sistema seguente: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | Stringa che rappresenta il numero di versione principale del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | Stringa che rappresenta il numero di versione secondario del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | Stringa che rappresenta la piattaforma del sistema operativo. I valori possibili della proprietà **Data** sono "1" per indicare un sistema Windows non supportato e "2" per indicare un sistema Windows supportato.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | Stringa che rappresenta la versione del sistema operativo. Il formato di questa stringa è *MajorVersion*. *MinorVersion*. *BuildNumber*. Ad esempio, "5.2.3790" per Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | Stringa che rappresenta l'architettura del processore del sistema operativo. Per un elenco di valori, vedere il membro **wProcessorArchitecture** della struttura [**delle \_ informazioni di sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | Stringa che rappresenta il tipo di prodotto. Per un elenco di valori, vedere il membro **wProductType** della struttura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv4 su cui è attualmente in ascolto lo stack RDP della macchina virtuale guest. Se lo stack RDP non è attualmente in esecuzione, la stringa sarà vuota. L'elenco viene aggiornato automaticamente ogni volta che una modifica della configurazione TCP/IP influiscono sullo stack RDP nella macchina virtuale guest. Ogni indirizzo è rappresentato nella notazione decimale del punto.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv6 su cui è attualmente in ascolto lo stack RDP della macchina virtuale guest. Se lo stack RDP non è attualmente in esecuzione, la stringa sarà vuota. L'elenco viene aggiornato automaticamente ogni volta che una modifica della configurazione TCP/IP influiscono sullo stack RDP nella macchina virtuale guest. Ogni indirizzo è rappresentato nella notazione esadecimale con due punti.<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | Stringa che rappresenta il numero di versione principale dell'Service Pack più recente installato nel sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | Stringa che rappresenta il numero di versione secondario del Service Pack più recente installato nel sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | Stringa che rappresenta i gruppi di prodotti disponibili nel sistema. Questa stringa è una combinazione dei valori del membro **wSuiteMask** della struttura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Origine**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Origine dei dati.



| Valore                                                                        | Significato                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | "HostExchangeItems" quando viene eseguito il push dall'host.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | "GuestExchangeItems" quando viene eseguito il push dalla macchina virtuale guest.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | "GuestIntrinsicExchangeItems" quando viene popolato automaticamente dalla macchina virtuale guest.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Indica che l'elemento è solo host e non è condiviso con la macchina virtuale guest. Utilizzato con la proprietà **HostOnlyItems** della classe [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ KvpExchangeDataItem di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ManagementName CIM**](cim-managedelement.md)
</dt> <dt>

[**\_ManagementName CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

