---
description: La classe \_ Win32 ServerFeature rappresenta le funzionalità installate in un computer che esegue Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Classe Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312138"
---
# <a name="win32_serverfeature-class"></a>Classe ServerFeature Win32 \_

\[La **classe \_ ServerFeature Win32** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece le classi [del provider ServerManager Deploymentprovider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]

La **classe \_ Win32 ServerFeature** rappresenta le funzionalità installate in un computer che esegue Windows Server.

Questa classe può essere utilizzata da sviluppatori e amministratori che devono automatizzare il processo di determinazione delle funzionalità installate in un set di computer server. Le istanze di questa classe non sono disponibili nei computer client.

## <a name="syntax"></a>Sintassi

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Members

La **classe \_ ServerFeature Win32** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ServerFeature Win32** dispone di queste proprietà.

<dl> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**Chiave**](key-qualifier.md), [**Non \_ Null**](optional-qualifiers.md)
</dt> </dl>

ID funzionalità del server. L'elenco seguente mostra i valori possibili della proprietà ID:



Valore

Nome

1

[Server applicazioni](/windows)

2

Server Web (IIS)

3

[Servizi flussi multimediali](/windows)

5

Server fax

6

Servizi file e iSCSI<br/> [modifica del nome](/windows)<br/>

7

Servizi di stampa e digitalizzazione<br/> [modifica del nome](/windows)<br/>

8

[Active Directory Federation Services](/windows)

9

Active Directory Lightweight Directory Services

10

Active Directory Domain Services

11

[Servizi UDDI](/windows)<br/>

12

[Server DHCP](/windows)

13

[DNS Server](/windows)

14

Servizi di accesso e criteri di rete

16

Servizi certificati Active Directory

17

Active Directory Rights Management Services

18

[Servizi Desktop remoto](/windows)<br/> [modifica del nome](/windows)<br/>

19

Servizi di distribuzione Windows

20

Hyper-V

21

[Windows Server Update Services](/windows)

33

[Clustering di failover](/windows)

34

[Bilanciamento del carico di rete](/windows)

36

[.NET Framework 3.5.1](/windows)<br/> [modifica del nome](/windows)<br/>

37

[Gestione risorse di sistema Windows](/windows)

38

Servizio LAN Wireless

39

[Windows Funzionalità di backup del server](/windows)

40

Server WINS

41

Servizio Attivazione dei processi Windows

42

[Assistenza remota](/windows)

43

Servizi TCP/IP semplificati

44

[Client Telnet](/windows)

45

[Server Telnet](/windows)

46

[Sottosistema per applicazioni basate su Unix](/windows)

47

Proxy RPC su HTTP

48

Server SMTP

49

accodamento messaggi

51

[Database interno di Windows](/windows)

52

[Archiviazione Manager per SAN](/windows)

53

Monitoraggio porta LPR

55

[Internet Storage Name Server](/windows)

57

[Multipath I/O](/windows)

58

Client TFTP

59

[Servizi SNMP](/windows)

60

[Removable Archiviazione Manager](/windows)

61

Crittografia unità BitLocker

62

[Servizi per file system di rete](/windows)

63

Client di stampa Internet

64

[Protocollo PNRP (Peer Name Resolution Protocol)](/windows)

65

Connection Manager Administration Kit

66

[Windows PowerShell](/windows)<br/>

67

[Strumenti di amministrazione remota del server](/windows)

68

[Servizio audio/video Windows di qualità](/windows)

69

[Gestione Criteri di gruppo](/windows)

71

[Servizio di indicizzazione](/windows)

72

[Gestione risorse file server](/windows)

73

Compressione differenziale remota

310

Servizi di riconoscimento della grafia<br/>

320

[Strumenti di migrazione per Windows Server](/windows)<br/>

321

[Estensione IIS di Gestione remota Windows](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[Console Gestione DirectAccess](/windows)<br/>

335

[Servizio trasferimento intelligente in background (BITS)](/windows)<br/>

338

[XPS Viewer](/windows)<br/>

339

[Windows Biometric Framework](/windows)<br/>

340

Supporto WoW64<br/>

351

[Windows PowerShell Integrated Scripting Environment (ISE)](/windows)<br/>

352

Windows TIFF IFilter<br/>

404

[Windows Server Update Services](/windows)

409

[Server di Gestione indirizzi IP](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Servizio Windows Search](/windows)

438

[Client per NFS](/windows)

441

[Sblocco di rete via BitLocker](/windows)

442

[Estensione IIS OData gestione](/windows)

450

[.NET Framework 4.5 Advanced Services](/windows)

466

[Funzionalità di .NET Framework 4.5](/windows)

468

[Accesso remoto](/windows)<br/>

477

[Interfacce utente e infrastruttura](/windows)

478

[Strumenti di gestione e infrastruttura grafica](/windows)

481

[Servizi file e archiviazione](/windows)

485

[Esperienza Windows Server Essentials](/windows)

488

[Esecuzione diretta](/windows)

Servizi file - Servizi ruolo (6)

Valore

Nome

100

[file system distribuito](/windows)

101

Spazio dei nomi DFS

102

Replica DFS

103

[Servizio Replica file](/windows)

104

[Gestione risorse file server](/windows)

105

[Servizi per file system di rete](/windows)

106

[Single Instance Storage (SIS)](/windows)

107

[Servizio Windows Search](/windows)

108

[Servizio di indicizzazione](/windows)

255

File Server

350

BranchCache per file di rete

431

[Server per NFS](/windows)<br/>

434

[Servizio agente File Server VSS](/windows)<br/>

435

[Server di destinazione iSCSI](/windows)<br/>

436

[Deduplicazione dati](/windows)<br/>

437

[Provider di servizi di Archiviazione destinazione iSCSI (provider hardware VDS e VSS)](/windows)

486

[Cartelle di lavoro](/windows)

Servizi di dominio Active Directory - Servizi ruolo (10)

Valore

Nome

110

[Controller di dominio di Active Directory](/windows)

111

[Gestione delle identità per Unix](/windows)

112

[Server per Network Information Services](/windows)

113

[Sincronizzazione delle password](/windows)

294

[Strumenti di amministrazione remota del server](/windows)

Streaming multimediale - Servizi ruolo (3)

Valore

Nome

120

[Windows Server dei contenuti multimediali](/windows)

121

[Amministrazione basata sul Web](/windows)

122

[Agente di registrazione](/windows)

ADFS - Servizi ruolo (8)

Valore

Nome

125

[Active Directory Federation Services](/windows)

126

[Servizio federativo criteri](/windows)

127

[Agenti Web ADFS](/windows)

128

[Agente in grado di riconoscere attestazioni](/windows)

129

[Windows Agente basato su token](/windows)

Servizi Desktop remoto - Servizi ruolo (18)

Valore

Nome

130

Host sessione Desktop remoto<br/> [modifica del nome](/windows)<br/>

131

[Servizio licenze Desktop remoto](/windows)<br/> [modifica del nome](/windows)<br/>

132

Gateway Desktop remoto<br/> [modifica del nome](/windows)<br/>

133

Gestore connessione Desktop remoto<br/> [modifica del nome](/windows)<br/>

134

Accesso Web Desktop remoto<br/> [modifica del nome](/windows)<br/>

322

Host di virtualizzazione Desktop remoto<br/>

Desktop remoto Virtualization Host - Servizi ruolo (322)

Valore

Nome

325

[Servizi di base](/windows)<br/>

327

[Desktop remoto grafica virtuale](/windows)<br/>

Servizi di stampa e digitalizzazione - Servizi ruolo (7)

Valore

Nome

135

Server di stampa

136

Stampa Internet

137

Servizio di stampa LPD

328

[Server Digitalizzazione distribuita](/windows)<br/>

Server Web (IIS) - Servizi ruolo (2)

Valore

Nome

140

Server web

141

Funzionalità HTTP comuni

142

Contenuto statico

143

Documento predefinito

144

Esplorazione della directory

145

Errori HTTP

146

Reindirizzamento HTTP

147

Sviluppo applicazioni

148

ASP.NET

149

Estendibilità .NET

150

ASP

151

CGI

152

Estensioni ISAPI

153

Filtri ISAPI

154

Server Side Includes

155

Integrità e diagnostica

156

Registrazione HTTP

157

Strumenti di registrazione

158

Monitoraggio richieste

159

Traccia

160

Registrazione personalizzata

161

Registrazione ODBC

162

Sicurezza

163

Autenticazione di base

164

Autenticazione di Windows

165

Autenticazione del digest

166

Autenticazione mapping certificati client

167

Autenticazione mapping certificati client IIS

168

Autorizzazione URL

169

Filtro richieste

170

Restrizioni ip e dominio

171

Prestazioni

172

Compressione contenuto statico

173

Compressione contenuto dinamico

174

Strumenti di gestione

175

Console di gestione IIS

176

Script e strumenti di gestione IIS

177

Servizio di gestione

178

Compatibilità Gestione IIS 6

179

Compatibilità Metabase IIS 6

180

Compatibilità WMI IIS 6

181

Strumenti di scripting di IIS 6

182

Console di gestione IIS 6

183

Servizio di pubblicazione FTP<br/>

184

Server FTP

185

Console di gestione FTP<br/>

314

Pubblicazione WebDAV

316

Servizio FTP<br/>

317

Estendibilità FTP<br/>

336

HWC (Hostable Web Core) di IIS<br/>

413

[ASP.NET 4.5](/windows)

414

[Estendibilità .NET 4.5](/windows)

445

[appialization](/windows)

446

[Supporto certificato SSL centralizzato](/windows)

447

[Protocollo WebSocket](/windows)

Accodamento messaggi - Funzionalità (49)

Valore

Nome

190

Servizi di accodamento messaggi

191

Message Queuing Server

192

Integrazione servizio directory

193

Trigger di accodamento messaggi

194

Supporto HTTP

195

Servizio di routing

196

[Windows client di Windows 2000](/windows)<br/>

197

Proxy DCOM di Accodamento messaggi

228

Supporto del multicasting

Servizi certificati Active Directory - Servizi ruolo (16)

Valore

Nome

200

Autorità di certificazione

201

Registrazione Web Autorità di certificazione

202

Risponditore online

204

Servizio Registrazione dispositivi di rete

318

[Servizio Web di registrazione certificati](/windows)<br/>

319

[Servizio Web di informazioni sulle registrazioni di certificati](/windows)<br/>

Criteri di rete e Access Services - Servizi ruolo (14)

Valore

Nome

205

[Server dei criteri di rete](/windows)

206

[VPN](#vpn)

207

[Connessione Access Services](/windows)

208

[Routing](#routing)

210

[Autorità registrazione integrità](/windows)

250

[Protocollo di autorizzazione delle credenziali host](/windows)

Servizi UDDI - Servizi ruolo (11)

Valore

Nome

215

[Applicazione Web servizi UDDI](/windows)<br/>

216

[Database di Servizi UDDI](/windows)<br/>

Windows Servizio attivazione processo - Servizi ruolo (41)

Valore

Nome

217

API di configurazione

218

Ambiente .NET

219

Modello di processo

.NET Framework 3.5.1 - Funzionalità (36)

Valore

Nome

220

.NET Framework 3.5.1<br/> [modifica del nome](/windows)<br/>

221

Attivazione di WCF

222

Attivazione HTTP

223

Attivazione non HTTP

227

XPS Viewer<br/>

Servizi SNMP - Funzionalità (59)

Valore

Nome

224

[Servizio SNMP](/windows)

225

[SNMP WMI Provider](/windows)

Servizi applicazioni - Servizi ruolo

Valore

Nome

230

[.NET Framework 3.5.1](/windows)<br/> [modifica del nome](/windows)<br/>

231

[Supporto server Web (IIS)](/windows)

232

[Accesso alla rete COM+](/windows)

233

[Condivisione delle porte TCP](/windows)

234

[Windows Supporto del servizio di attivazione dei processi](/windows)

235

[Attivazione HTTP](/windows)

236

[Attivazione di Accodamento messaggi](/windows)

237

[Attivazione TCP](/windows)

238

[Attivazione di named pipe](/windows)

239

[Transazioni distribuite](/windows)

240

[Transazioni remote in ingresso](/windows)

241

[Transazioni remote in uscita](/windows)

242

[Transazioni WS-Automatic](/windows)

353

[Estensioni del server applicazioni per .NET 4.0](/windows)<br/>

Windows Servizi di distribuzione - Ruolo (19)

Valore

Nome

251

Server di distribuzione

252

Server di trasporto

Active Directory Rights Management Services - Servizi ruolo (17)

Valore

Nome

253

Server AD RMS (Active Directory Rights Management Services)

254

Supporto federazione identità

Strumenti di amministrazione remota del server (67)

Valore

Nome

256

[Strumenti di amministrazione ruoli](/windows)

257

[Strumenti di Servizi di dominio Active Directory](/windows)<br/> [modifica del nome](/windows)<br/>

258

[AD LDS Snap-Ins e Command-Line strumenti](/windows)<br/> [modifica del nome](/windows)<br/>

259

Strumenti per Servizi certificati Active Directory

260

[Servizi di accesso e criteri di rete](/windows)

261

strumenti Servizi di stampa e digitalizzazione<br/> [modifica del nome](/windows)<br/>

262

[Active Directory Rights Management Services](/windows)

263

[Strumenti per Servizi Desktop remoto](/windows)<br/> [modifica del nome](/windows)<br/>

264

Windows Strumenti di Servizi di distribuzione

265

[Strumenti di amministrazione funzionalità](/windows)

266

BitLocker Drive Encryption Tools

267

Strumenti per Estensioni server BITS

268

[Strumenti per Clustering di failover](/windows)

269

Strumenti per Bilanciamento carico di rete

270

Strumenti del server SMTP

273

[Strumenti per Server DNS](/windows)

277

Strumenti per Servizi file

278

strumenti file system distribuito

279

Strumenti per Gestione risorse file server

280

[Servizi per gli strumenti del file system di rete](/windows)

281

Strumenti server Web (IIS)

284

[Desktop remoto host sessione di lavoro](/windows)<br/> [modifica del nome](/windows)<br/>

285

Desktop remoto gateway<br/> [modifica del nome](/windows)<br/>

286

Desktop remoto strumenti di gestione delle licenze<br/> [modifica del nome](/windows)<br/>

288

Strumenti del server fax

290

Strumenti del server WINS

291

[Strumenti di Servizi UDDI](/windows)<br/>

292

Strumenti dell'autorità di certificazione

293

Strumenti risponditore online

297

[server per NIS strumenti](/windows)

299

[Snap-in e strumenti da riga di comando di Servizi di dominio Active Directory](/windows)<br/> [modifica del nome](/windows)<br/>

300

[Centro di amministrazione di Active Directory](/windows)

301

Strumenti di Hyper-V

323

[Visualizzatore password di ripristino di BitLocker](/windows)<br/>

326

[BitLocker Drive Encryption Administration Utilities](/windows)<br/>

329

[Strumenti per Servizi di dominio Active Directory e AD LDS](/windows)<br/>

330

Centro di amministrazione di Active Directory<br/>

331

[Modulo di Active Directory per Windows PowerShell](/windows)<br/>

337

[Connessione Desktop remoto Broker Tools](/windows)<br/>

410

[Gestione indirizzi IP client (Gestione indirizzi IP)](/windows)

450

[Modulo Hyper-V per Windows PowerShell](/windows)

462

[Active Directory Rights Management Services Strumenti](/windows)

465

[Share and Archiviazione Management Tool](/windows)

471

[Strumenti di Gestione Accesso remoto](/windows)

472

[Modulo Accesso remoto per Windows PowerShell](/windows)

473

[Interfaccia utente grafica e strumenti Command-Line accesso remoto](/windows)

474

[Strumenti di Windows Server Update Services](/windows)

476

[Desktop remoto strumenti di diagnostica delle licenze](/windows)

479

[Strumenti SNMP](/windows)

480

[Strumenti di attivazione dei contratti multilicenza](/windows)

Windows Backup server - Funzionalità (39)

Valore

Nome

296

[Windows Server Backup](/windows)

297

[Strumenti da riga di comando](/windows)

Servizi di riconoscimento della grafia - Funzionalità (310)

Valore

Nome

311

[Supporto input penna](/windows)<br/>

312

[Riconoscimento della grafia](/windows)<br/>

Servizio trasferimento intelligente in background (BITS) - Funzionalità (335)

Valore

Nome

54

Estensione del server IIS

332

[Compact Server](/windows)<br/>

Supporto wow64 - Funzionalità (340)

Valore

Nome

341

[WoW64](#wow64)<br/>

342

[WoW64 per .NET Framework 2.0 e Windows PowerShell](/windows)<br/>

343

[WoW64 per .NET Framework 2.0](/windows)<br/>

344

[WoW64 per PowerShell](/windows)<br/>

345

[WoW64 per .NET Framework 3.0 e 3.5](/windows)<br/>

346

[WoW64 per servizi di stampa](/windows)<br/>

347

[WoW64 per clustering di failover](/windows)<br/>

348

[WoW64 per Input Method Editor](/windows)<br/>

349

[WoW64 for Subsystem for UNIX-based Applications](/windows)<br/>

Interfacce utente e infrastruttura - Servizi ruolo (447)

Valore

Nome

35

[Esperienza desktop](/windows)

99

[Shell grafica server](/windows)

Windows Server Update Services - Funzionalità (404)

Valore

Nome

405

[API e cmdlet di PowerShell](/windows)

406

[SQL Server Connettività](/windows)

407

[Servizi WSUS](/windows)

408

[Interfaccia utente Management Console](/windows)

449

[Connettività WID](/windows)

Windows PowerShell - Funzionalità (417)

Valore

Nome

411

[Windows PowerShell 2.0](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Accesso Web di Windows PowerShell](/windows)

1000

[Windows PowerShell Desired State Configuration servizio](/windows)

.NET Framework 4.5 - Funzionalità (418)

Valore

Nome

419

[.NET Framework 4.5 Extended](/windows)

420

[Servizi WCF](/windows)

421

[Attivazione HTTP](/windows)

422

[Attivazione di Accodamento messaggi (MSMQ)](/windows)

423

[Attivazione named pipe](/windows)

424

[Attivazione TCP](/windows)

425

[Condivisione delle porte TCP](/windows)

429

[ASP.NET 4.5](/windows)

Accesso remoto - Ruolo (468)

Valore

Nome

469

[DirectAccess e VPN (RAS)](/windows)

470

[Routing](#routing)

Servizi file e Archiviazione - Ruolo (481)

Valore

Nome

482

[Servizi di archiviazione](/windows)

484

[Strumenti di gestione del cluster di failover](/windows)



 

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome visualizzato della funzionalità server, ad esempio "File server", "Server di stampa" o "Esperienza desktop".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Numero ID della funzionalità del server padre. Questa proprietà è 0 se la funzionalità rappresentata dall'istanza corrente della classe non ha una funzionalità padre.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sulle funzionalità del server, Windows Panoramica tecnica di [Server Manager Server 2008.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10))

Le aziende che non usano software di gestione che segnala le funzionalità del server, ad esempio System Center Operations Manager con Management Pack installati, possono ottenere tali informazioni tramite una query sulla **classe \_ ServerFeature Win32.**

È possibile usare le funzionalità remote di WMI o WinRM per ottenere informazioni sulle funzionalità del server dai server remoti. Per altre informazioni sulle connessioni WMI DCOM remote, vedere [Connessione a WMI in un computer remoto.](connecting-to-wmi-on-a-remote-computer.md) Per altre informazioni su WinRM, vedere Windows Remote Management (Gestione remota Windows).

Windows Server 2012: **Win32 \_ ServerFeature** è stato deprecato. Per accedere alle informazioni sulle funzionalità di Windows Server a livello di codice, è possibile [usare i cmdlet Server Manager .](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))

### <a name="windows-server-2012-r2"></a>R2 per Windows Server 2012

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Server applicazioni
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Flusso Servizi multimediali
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Servizi Desktop remoto
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Bilanciamento carico di rete
</dt> <dd>

Non più supportato

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Funzionalità
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Sistema Resource Manager
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Funzionalità di backup del server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistenza remota
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Sottosistema per applicazioni basate su Unix
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Database interno di Windows
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Archiviazione Manager per san
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Server dei Archiviazione Internet
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Servizi SNMP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servizi per file system di rete
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione remota del server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Esperienza Windows video audio
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Criteri di gruppo gestione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servizio di indicizzazione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File server Resource Manager (FSRM)
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Strumenti di migrazione server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>Branchcache
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console di gestione DirectAccess
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servizio trasferimento intelligente in background (BITS)
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Supporto di WoW64
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Gestione indirizzi IP server (Gestione indirizzi IP)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Servizio di ricerca
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client per NFS
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Sblocco rete BitLocker
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Estensione IIS OData di gestione
</dt> <dd>

Aggiunta

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services
</dt> <dd>

Aggiunta

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Funzionalità
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfacce utente e infrastruttura
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Infrastruttura e strumenti di gestione grafica
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Servizi file e Archiviazione
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Esperienza di Server Essentials
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>file system distribuito
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servizi per file system di rete
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Istanza singola Archiviazione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Servizio di ricerca
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servizio di indicizzazione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Provider di Archiviazione destinazione iSCSI (provider hardware VDS e VSS)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Dominio di Active Directory controller
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gestione delle identità per Unix
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server per Network Information Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronizzazione delle password
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Server multimediale
</dt> <dd>

Non più supportata.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Amministrazione basata sul Web
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente di registrazione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Servizio federativo
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Servizio federativo criteri
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web agent
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Agente basato su token
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Desktop remoto licenze
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Server dei criteri di rete
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>Vpn
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Connessione Access Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autorità di registrazione integrità
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocollo di autorizzazione delle credenziali host
</dt> <dd>

Non più supportato

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Servizio SNMP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider
</dt> <dd>

Non più supportato

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Supporto del server Web (IIS)
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accesso alla rete COM+
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Condivisione delle porte TCP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Supporto del servizio di attivazione dei processi
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Attivazione HTTP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Attivazione di Accodamento messaggi
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Attivazione TCP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Attivazione di named pipe
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transazioni distribuite
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transazioni remote in ingresso
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transazioni remote in uscita
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transazioni automatiche WS
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Estensioni del server applicazioni per .NET 4.0
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione dei ruoli
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Strumenti di Servizi di dominio Active Directory
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins e Command-Line strumenti
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Criteri di rete e Access Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Servizi Desktop remoto strumenti
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione delle funzionalità
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Strumenti di clustering di failover
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Strumenti server DNS
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Servizi per gli strumenti del file system di rete
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Strumenti del server Web (IIS)
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>server per NIS strumenti
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Strumenti di Snap-Ins e Command-Line Servizi di dominio Active Directory
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Servizi di dominio Active Directory e AD LDS strumenti
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Connessione Desktop remoto Broker Tools
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Gestione indirizzi IP client (Gestione indirizzi IP)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Modulo Hyper-V per Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Strumento
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Archiviazione Management Tool
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Strumenti di gestione accesso remoto
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Modulo di accesso remoto per Windows PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Interfaccia utente grafica e strumenti Command-Line Accesso remoto
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Strumenti
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Desktop remoto strumenti di diagnostica delle licenze
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Strumenti SNMP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Strumenti di attivazione dei contratti multilicenza
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Strumenti da riga di comando
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Supporto input penna
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Riconoscimento della grafia
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 per .NET Framework 2.0 e PowerShell
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 per .NET Framework 2.0
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 per PowerShell
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 per .NET Framework 3.0 e 3.5
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 per Servizi di stampa
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 per clustering di failover
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 per Input Method Editor
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Esperienza desktop
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell grafica server
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API e cmdlet di PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connettività
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Servizi WSUS
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Interfaccia utente Management Console
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Connettività WID
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Accesso Web
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration servizio
</dt> <dd>

Aggiunta

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Servizi WCF
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Attivazione HTTP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Attivazione di Accodamento messaggi (MSMQ)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Attivazione named pipe
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Attivazione TCP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Condivisione delle porte TCP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5
</dt> <dd>

Aggiunta

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Estendibilità .NET 4.5
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess e VPN (RAS)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Archiviazione Servizi
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Strumenti di gestione del cluster di failover
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Strumenti
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inizializzazione dell'applicazione
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Supporto centralizzato dei certificati SSL
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente in grado di riconoscere attestazioni
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Desktop remoto host di sessione
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocollo WebSocket
</dt> <dd>

non più supportato

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accesso alla rete COM+
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Modifica del nome dei servizi file e iSCSI
</dt> <dd>

Modificato in Servizi file

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfacce utente e infrastruttura
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server per NFS
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Servizio VsS Agent per file server
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Server di destinazione iSCSI
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Deduplicazione dati
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro
</dt> <dd>

Rimosso

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Servizi di base
</dt> <dd>

Aggiunta solo per questa versione.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Desktop remoto grafica virtuale
</dt> <dd>

Aggiunta solo per questa versione

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Accesso remoto
</dt> <dd>

Aggiunta

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Servizi UDDI
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Sistema Resource Manager
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Gestione Archiviazione rimovibili
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Servizi di riconoscimento della grafia
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Estensione IIS di Gestione remota Windows
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console di gestione DirectAccess
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servizio trasferimento intelligente in background (BITS)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Framework biometrico
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Supporto di WoW64
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Servizio Replica file
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache per i file di rete
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Server Digitalizzazione distribuita
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Servizio pubblicazione FTP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console di gestione FTP
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Servizio FTP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Estendibilità FTP
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Web Core ospitabile di IIS
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Servizio Web di registrazione certificati
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Servizio Web di informazioni sulle registrazioni di certificati
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Applicazione Web servizi UDDI
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Database di Servizi UDDI
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Estensioni del server applicazioni per .NET 4.0
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Strumenti di Servizi UDDI
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Crittografia unità BitLocker di amministrazione
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Servizi di dominio Active Directory e AD LDS strumenti
</dt> <dd>

Non più supportato

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Servizi di dominio Active Directory e AD LDS strumenti
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro di amministrazione di Active Directory
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Modulo di Active Directory per Windows PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Connessione Desktop remoto Broker Tools
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 per .NET Framework 2.0 e Windows PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 per .NET Framework 2.0
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 per PowerShell
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 per .NET Framework 3.0 e 3.5
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 per Servizi di stampa
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 per clustering di failover
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 per Input Method Editor
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visualizzatore password di ripristino di BitLocker
</dt> <dd>

Aggiunta

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Servizi di stampa e digitalizzazione modifica del nome
</dt> <dd>

servizi di stampa denominati per questa versione

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Servizi Desktop remoto del nome
</dt> <dd>

denominato Servizi terminal in questa versione

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Modifica del nome delle funzionalità
</dt> <dd>

Funzionalità .NET Framework 3.0 denominate in questa versione

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Desktop remoto nome host sessione di lavoro
</dt> <dd>

Terminal Server denominato in questa versione

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Desktop remoto del nome della licenza
</dt> <dd>

Licenze TS denominate in questa versione

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Desktop remoto del nome del gateway
</dt> <dd>

Gateway TS denominato in questa versione

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Connessione Desktop remoto nome broker
</dt> <dd>

Denominato TS Session Broker in questa versione

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Desktop remoto Accesso Web del nome
</dt> <dd>

TS Accesso Web in questa versione

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework nome 3.5.1
</dt> <dd>

(220) Funzionalità di Net FX 3.0 denominate in questa versione

(230) Denominato Application Server Core in questa versione

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Modifica del nome degli strumenti di Servizi di dominio Active Directory
</dt> <dd>

Strumenti Active Directory Domain Services denominati in questa versione

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins e Command-Line modifica del nome degli strumenti
</dt> <dd>

Strumenti Active Directory Lightweight Directory Services denominati in questa versione

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Servizi di stampa e digitalizzazione nome degli strumenti di distribuzione
</dt> <dd>

Strumenti di Servizi di stampa denominati in questa versione

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Servizi Desktop remoto modifica del nome degli strumenti di distribuzione
</dt> <dd>

Strumenti di Servizi terminal denominati in questa versione

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Desktop remoto nome degli strumenti host della sessione
</dt> <dd>

Strumenti terminal server denominati in questa versione

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Desktop remoto del nome degli strumenti gateway
</dt> <dd>

Strumenti gateway TS denominati in questa versione

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Desktop remoto nome degli strumenti di gestione delle licenze
</dt> <dd>

Strumenti di gestione licenze TS denominati in questa versione

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Modifica del nome degli strumenti Snap-Ins e Command-Line Servizi di dominio Active Directory
</dt> <dd>

Strumenti del Controller di dominio Active Directory

</dd> </dl>

## <a name="examples"></a>Esempio

Lo script seguente visualizza i nomi di tutte le funzionalità del server nel computer denominato "FABRIKAM". Si noti che il computer di destinazione deve eseguire Windows Server 2008 o un sistema operativo server successivo.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

